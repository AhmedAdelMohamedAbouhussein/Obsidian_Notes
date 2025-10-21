
ip link
ip addr show
systemctl status sshd
lsblk
fdisk /dev/storagename			g/p/n/w/t

mkfs.fat -F32 /dev/sdb1
mkfs.ext4 /dev/sdb2
mkswap /dev/sdb3


cryptsetup luksFormat /dev/sdb4	encrypt a partition
cryptsetup open --type luks /dev/sdb4 main_lvm	access an encrypted lvm
pvcreate /dev/mapper/main_lvm		create a physical volumn to be using with lvm
vgcreate main_volgroup0 /dev/mapper/main_lvm     create volume group
lvcreate -L 30GB main_volgroup0 -n lv_root	create logical group
lvcreate -l 100%FREE -n lv_home main_volgroup0
lvdisplay

cryptsetup luksFormat /dev/sda1	encrypt a partition
cryptsetup open --type luks /dev/sda1 data_lvm	access an encrypted lvm
pvcreate /dev/mapper/data_lvm		create a physical volumn to be using with lvm
vgcreate data_volgroup0 /dev/mapper/data_lvm     create volume group
lvcreate -l 100%FREE -n lv_data data_volgroup0
lvdisplay

modprobe dm_mod
vgscan
vgchange -ay
mkfs.ext4 /dev/main_volgroup0/lv_root
mkfs.ext4 /dev/main_volgroup0/lv_home
mkfs.ext4 /dev/data_volgroup0/lv_data

mount /dev/main_volgroup0/lv_root /mnt
mkdir /mnt/boot
mount /dev/sdb2 /mnt/boot
mkdir /mnt/home
mount /dev/main_volgroup0/lv_home /mnt/home

mkdir /mnt/data
mount /dev/data_volgroup0/lv_data /mnt/data 

swapon /dev/sdb3

swapon --show


pacstrap -i /mnt base

# genfstab -U -p /mnt >> /mnt/etc/fstab
cat /mnt/etc/fstab

arch-chroot /mnt
passwd
useradd -m -G wheel -s /bin/bash User
passwd **** 
ln -sf /usr/share/zoneinfo/Africa/Cairo /etc/localtime
date
Vhwclock --systohc


pacman -S base-devel grub dosfstools  efibootmgr lvm2 mtools nano neovim networkmanager sudo plasma sddm linux linux-headers linux-lts linux-lts-headers linux-firmware 

answers: 1 2 2 1

pacman -S mesa libva-intel-driver libva-utils intel-ucode git fastfetch libreOffice Okular  dolphin konsole gwenview docker Firefox zram-generator

answers: 2

lspci
nano /etc/mkinitcpio.conf	and add to hooks (encrypt lvm2) in between block and filesystem 
nano /etc/locale.gen		uncomment en_US.UTF-8
locale-gen
nano /etc/locale.conf  and type LANG=en_US.UTF-8

nano /etc/hostname and type Arch Linux

#nano /etc/default/grub    
GRUB_CMDLINE_LINUX_DEFAULT="cryptdevice=/dev/sdb4:main_lvm root=/dev/main_volgroup0/lv_root quiet"
blkid /dev/sda1
nano /etc/crypttab
data_volgroup0-data_lvm UUID=282835e9-9dd1-4229-b7a9-996aa5f1626c none luks

mkdir /boot/EFI
mount /dev/sdb1 /boot/EFI

mkinitcpio -p linux
mkinitcpio -p linux-lts

grub-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
cp /usr/share/locale/en\@quot/LC_MESSAGES/grub.mo /boot/grub/locale/en.mo
grub-mkconfig -o /boot/grub/grub.cfg

systemctl enable NetworkManager sddm bluetooth

EDITOR=nano visudo uncomment %wheel All=(All) All
su AhmedAdel

exit
umount -R /mnt
swapoff -a
reboot



yay -S bpytop


### 1️⃣ Mount SSD (new system)

`# Root and home 
sudo mount /dev/main_volgroup0/lv_root /mnt/newroot 
sudo mkdir -p /mnt/newroot/home 
sudo mount /dev/main_volgroup0/lv_data /mnt/newroot/home  
# Boot and EFI 
sudo mkdir -p /mnt/newroot/boot 
sudo mount /dev/sda2 /mnt/newroot/boot 
sudo mkdir -p /mnt/newroot/boot/efi 
sudo mount /dev/sda1 /mnt/newroot/boot/efi`

---

### 2️⃣ Mount old HDD (old system)

sudo modprobe dm_mod 
sudo vgscan 
sudo vgchange -ay  
sudo mkdir -p /mnt/oldroot 
sudo mount /dev/main_volgroup0/lv_root /mnt/oldroot 
sudo mkdir -p /mnt/oldroot/home 
sudo mount /dev/main_volgroup0/lv_data /mnt/oldroot/home 
# Boot and EFI from old HDD 
sudo mkdir -p /mnt/oldroot/boot 
sudo mount /dev/sdb2 /mnt/oldroot/boot 
sudo mkdir -p /mnt/oldroot/boot/efi 
sudo mount /dev/sdb1 /mnt/oldroot/boot/efi`

---

### 3️⃣ Copy everything from old root to new root

`sudo rsync -aAXHv --exclude={"/dev/*","/proc/*","/sys/*","/tmp/*","/run/*","/mnt/*","/media/*","/lost+found"} /mnt/oldroot/ /mnt/newroot/`

---

### 4️⃣ Copy `/home` (preserve user data)

`sudo rsync -aAXHv /mnt/oldroot/home/ /mnt/newroot/home/`

---

### 5️⃣ Copy `/boot` and EFI

`sudo rsync -aAXHv /mnt/oldroot/boot/ /mnt/newroot/boot/ sudo rsync -aAXHv /mnt/oldroot/boot/efi/ /mnt/newroot/boot/efi/`

---

### 6️⃣ Generate fstab for SSD

`sudo genfstab -U /mnt/newroot > /mnt/newroot/etc/fstab`

---

### 7️⃣ Chroot into SSD

`sudo arch-chroot /mnt/newroot`

Inside chroot:

# Rebuild initramfs
mkinitcpio -P  
# Reinstall GRUB 
grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=Arch 
grub-mkconfig -o /boot/grub/grub.cfg 
# Enable swap 
swapon /dev/sda3`

Exit chroot and unmount:

`exit sudo umount -R /mnt/newroot sudo swapoff /dev/sda3`