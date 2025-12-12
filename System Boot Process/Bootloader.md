# 🧠 Bootloader

## 📖 Definition
A **bootloader** is a small program that runs immediately after the computer’s firmware (BIOS or UEFI) and is responsible for **loading the operating system kernel** into memory.

It acts as the **bridge between firmware and the OS**.

---

## ⚙️ Purpose
- Initializes hardware components after firmware.
- Locates the operating system kernel (like Linux or Windows).
- Loads the kernel into memory and starts the boot process.
- Allows the user to choose between multiple operating systems (in dual-boot setups).

---

## 🧩 Stages of Boot
1. **Firmware Stage (BIOS/UEFI)**  
   → Finds and executes the bootloader.
2. **Bootloader Stage**  
   → Loads kernel + initramfs (initial RAM filesystem).
3. **Kernel Stage**  
   → Kernel initializes system hardware & mounts root filesystem.
4. **User Space Initialization**  
   → System services start (`systemd`, `init`, etc.).

---

## 🧰 Common Bootloaders
| Bootloader | Description | Used in |
|-------------|--------------|---------|
| **GRUB (GNU GRand Unified Bootloader)** | Most common on Linux; supports multiple OSs | Arch, Ubuntu, Fedora |
| **systemd-boot** | Lightweight, UEFI-only bootloader integrated with `systemd` | Arch, Fedora (UEFI) |
| **rEFInd** | Graphical boot manager for UEFI systems | Dual-boot setups |
| **Windows Boot Manager (bootmgr)** | Default bootloader for Windows | Windows |

---

## 🧠 Example (GRUB on Linux)

```bash
grub-install /dev/sda
grub-mkconfig -o /boot/grub/grub.cfg
