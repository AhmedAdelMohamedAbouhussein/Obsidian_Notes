# ⚙️ Essential BIOS Settings for Linux (Arch Installation)

## 📘 Overview
Before installing Linux (especially Arch), it’s important to configure certain BIOS/UEFI settings to ensure **hardware compatibility**, **faster performance**, and **a successful boot**.

Below are the most important BIOS options explained.

---

## 🔑 1. Secure Boot

### 🧠 What It Is
**Secure Boot** is a UEFI security feature that only allows bootloaders and operating systems **digitally signed with trusted keys (usually Microsoft’s)** to start.  
It helps protect against malware that tries to run before your OS boots.

### ⚙️ On Linux (Arch)
- **Arch Linux** does **not** support Secure Boot by default.  
- You can enable it manually later by **signing the kernel and bootloader** with your own keys — but this is an advanced setup.

### ✅ Recommendation
> Disable **Secure Boot** during installation.  
This avoids boot errors and simplifies the setup process.

---

## 🔑 2. SATA Mode

### 🧠 What It Is
Controls how your motherboard communicates with storage drives (HDDs and SSDs).

### ⚙️ Common Modes
| Mode                                          | Description                                                           | Recommended                    |
| --------------------------------------------- | --------------------------------------------------------------------- | ------------------------------ |
| **AHCI (Advanced Host Controller Interface)** | Modern standard, supports NCQ, TRIM, and SSD features.                | ✅ Best for Linux & SSDs        |
| **RAID**                                      | Used for combining multiple drives — may require proprietary drivers. | ❌ Not ideal for Linux installs |
| **IDE (Legacy)**                              | Outdated compatibility mode.                                          | ❌ Avoid                        |

### ✅ Recommendation
> Set **SATA Mode = AHCI**  
It ensures optimal disk performance and compatibility with Linux.

---

## 🔑 3. Boot Priority

### 🧠 What It Is
Determines which device the BIOS tries to boot from first (USB, HDD, SSD, etc.).

### ⚙️ During Installation
- Set your **USB drive** (the one containing Arch ISO) as **first** in boot order.
- Boot the system and install Arch.

### ⚙️ After Installation
- Change boot order back so that your **main drive (with Arch bootloader)** is **first**.
- This ensures your system boots Arch automatically without needing the USB.

---

## 🔧 4. Other Optional Settings

### ⚡ Fast Boot
- Skips some hardware checks to speed up startup.
- Can cause issues with **USB detection** or **booting installers**.
- **Recommendation:** ❌ Disable during installation.

### 🧩 Virtualization (Intel VT-x / AMD-V)
- Enables running **virtual machines**, **Docker**, **WSL2**, or **emulators** efficiently.
- **Recommendation:** ✅ Enable it — especially useful for developers and power users.

---

## 💡 Summary

| Setting            | Recommended Value    | Why                              |
| ------------------ | -------------------- | -------------------------------- |
| **Secure Boot**    | Disabled             | Easier Linux installation        |
| **SATA Mode**      | AHCI                 | Best performance & compatibility |
| **Boot Priority**  | USB first (then SSD) | Proper boot order                |
| **Fast Boot**      | Disabled             | Prevent detection issues         |
| **Virtualization** | Enabled              | Needed for VMs & WSL             |

---

📌 Final Recommended Setup for Arch (UEFI)

Boot Mode: UEFI ✅

Legacy Option ROMs: Disabled ✅

Secure Boot: Disabled ✅

SATA Mode: AHCI ✅

Boot Order: USB first, then HDD/SSD