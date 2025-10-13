### 🔹 BIOS (Basic Input/Output System)

- **Old firmware interface** used before the OS starts.
    
- Stored in the **motherboard’s ROM chip**.
    
- Loads the bootloader from the **first sector (MBR)** of the disk.
    
- **Text-based interface**, navigated with keyboard only.
    
- **Limited to 16-bit mode**, and can only boot from drives **≤ 2 TB**.
    
- Doesn’t support **secure boot**, **mouse input**, or modern GUI.
    

### 🔹 UEFI (Unified Extensible Firmware Interface)

- **Modern replacement** for BIOS.
    
- Stored in the motherboard’s **NVRAM** or flash storage.
    
- Uses a small **EFI System Partition (ESP)** on the disk to store bootloaders.
    
- **Graphical interface** (mouse & keyboard supported).
    
- Supports **Secure Boot**, **network boot**, and drives **> 2 TB**.
    
- Much **faster boot times** and more **modular**.
    
- Can boot in both **UEFI mode** and **Legacy (BIOS compatibility) mode**.

![[Pasted image 20251013225209.png]]