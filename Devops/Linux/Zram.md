# ZRAM Swap Setup on Arch Linux

## 📘 Overview
**ZRAM** allows you to create **compressed swap in RAM**, which is faster than using a traditional HDD swap.  
It is especially useful for systems with **limited RAM** or for improving responsiveness on Linux desktops.

This guide explains step-by-step how to configure zram while keeping the HDD swap as a fallback.


🧠 What really happens inside zram

Let’s say you open an app that needs 1 GB of RAM.

Normally (no zram):

App data: 1 GB → stored directly in RAM → 1 GB used


With zram enabled:

Linux keeps the active parts of that app (the code and data it’s actively using) in normal RAM.

It takes the inactive or less-used pages (for example, old data, background resources, etc.)
and compresses them into zram.

Let’s assume those inactive pages total 500 MB before compression.

If zstd compresses them at a 2:1 ratio, they now only take 250 MB of real RAM space.

So total RAM actually used becomes:

Active part in normal RAM: 500 MB
Compressed part in zram: 250 MB (was 500 MB)
Total real usage: 750 MB

📊 Compression ratios vary

Typical ratio: 1.5 : 1 to 2.5 : 1

Highly compressible data (text, cached stuff): up to 3 : 1

Already-compressed data (videos, images): ~1 : 1 (no gain)

So savings vary depending on what your system is doing.
---

## 🧩 Step 1: Install zram support

	sudo pacman -S zram-generator

### Explanation

- `zram-generator` is a systemd service that automatically creates **zram devices** for swap.
    
- No kernel recompilation is required; it works with stock Arch kernels.
    

---

## 🧩 Step 2: Disable the old HDD swap (temporarily)

`sudo swapoff -a`

### Explanation

- Temporarily disables all swap devices.
    
- Necessary to safely configure zram and update `/etc/fstab`.
    

---

## 🧩 Step 3: Edit /etc/fstab for HDD swap priority

`sudo nano /etc/fstab`

- Find the line for your HDD swap, e.g.:
    

`/dev/sda2 none swap sw 0 0`

- Change it to:
    

`/dev/sda2 none swap sw,pri=10 0 0`

### Explanation

- `pri=10` → Lowers priority so zram swap is used first.
    
- Your HDD swap is **still available** but only used when RAM swap is exhausted.
    

---

## 🧩 Step 4: Create zram configuration

`sudo nano /etc/systemd/zram-generator.conf`

- Add the following:
    

`[zram0] zram-size = ram compression-algorithm = zstd swap-priority = 100`

### Explanation

- `zram-size = ram` → Uses up to full physical RAM for compressed swap.
    
- `compression-algorithm = zstd` → Fast and efficient compression.
    
- `swap-priority = 100` → Ensures zram swap is used **before** HDD swap.
    

---

## 🧩 Step 5: Enable and start zram

`sudo systemctl enable --now systemd-zram-setup@zram0`

### Explanation

- Enables the zram generator service at boot.
    
- `--now` starts it immediately without rebooting.
    

---

## 🧩 Step 6: Reactivate all swap devices

`sudo swapon -a`

### Explanation

- Re-enables all swap devices including **HDD swap and zram**.
    
- System will now prioritize zram (priority 100) over HDD swap (priority 10).
    

---

## 🧩 Step 7: Verify zram is active

`swapon --show`

Expected output:

`NAME       TYPE      SIZE  USED PRIO /dev/zram0 zram      4G    0B   100 /dev/sda2  partition 8G    0B   10`

### Explanation

- Confirms that zram is active and has **higher priority** than HDD swap.
    

---

## 🧩 Step 8: Reduce swap aggressiveness

`echo 'vm.swappiness=10' | sudo tee /etc/sysctl.d/99-swappiness.conf sudo sysctl --system`

### Explanation

- `vm.swappiness=10` → Tells Linux **to use swap less aggressively**, keeping more processes in RAM.
    
- Improves performance and reduces unnecessary swapping.
    

---

## 🧩 Step 9: Use Preload to cache common apps

`sudo pacman -S preload sudo systemctl enable --now preload`

### Explanation

- **Preload** is a background service that **learns which apps you use frequently**.
    
- It **preloads them into RAM** at startup, reducing app launch times.
    
- Works automatically; no configuration needed.
    

---

## ✅ Final Result

- 4 GB physical RAM
    
- ~4 GB fast **zram swap** (priority 100)
    
- 8 GB slower **HDD swap** (priority 10)
    
- Reduced swap usage (`swappiness=10`)
    
- Frequently used apps load faster with **Preload**
    

> System feels **snappy and responsive**, even under heavy load.