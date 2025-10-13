# 10 Partition Formats Across Operating Systems

## 📘 Overview
Different operating systems use different **partition tables** and **filesystem formats**. Understanding these is essential for dual-boot setups, data sharing, and disk management.

---

## 🧠 1. Partition Tables: MBR vs GPT

### MBR (Master Boot Record)
- **Max Disk Size**: 2 TB  
- **Partition Limit**: 4 primary partitions (can use extended partitions for more)  
- **Boot Mode**: Legacy BIOS  
- Stores bootloader and partition info in the first sector.  
- **Limitations**:  
  - Cannot handle disks larger than 2 TB.  
  - No redundancy; if MBR is corrupted, data may be lost.  

### GPT (GUID Partition Table)
- **Max Disk Size**: 9.4 ZB (practically unlimited)  
- **Partition Limit**: 128 partitions (Windows default)  
- **Boot Mode**: UEFI  
- Stores multiple copies of partition info (redundancy) and uses **GUIDs**.  
- Recommended for modern systems and large drives.  

> ✅ **Rule of thumb:** Use GPT with UEFI, MBR with legacy BIOS.  

---

## 🧠 2. Filesystem Types by OS

| OS          | Common Filesystems                 | Notes                                                                                         |
| ----------- | ---------------------------------- | --------------------------------------------------------------------------------------------- |
| **Linux**   | ext4, ext3, ext2, Btrfs, XFS, F2FS | ext4 is default; Btrfs supports snapshots; XFS for large filesystems; F2FS optimized for SSDs |
| **Windows** | NTFS, FAT32, exFAT                 | NTFS is default; FAT32 for compatibility; exFAT for external drives                           |
| **macOS**   | APFS, HFS+                         | APFS is default for macOS 10.13+; HFS+ older systems                                          |

---

### 🔹 Linux Filesystems

- **ext4 (Fourth Extended Filesystem)**
    
    - **Default** for most Linux distributions.
        
    - **Features**: Journaling (logs metadata to prevent corruption), large file support, high reliability.
        
    - **Pros**: Very stable, well-tested, compatible with almost all Linux tools.
        
    - **Cons**: Lacks advanced features like snapshots and compression (compared to Btrfs).
        
    - **Use Case**: Root (`/`), home directories, and standard Linux partitions.
        
- **Btrfs (B-tree Filesystem)**
    
    - Advanced filesystem with **copy-on-write (COW)**, snapshots, and compression.
        
    - **Features**: Transparent compression, checksums for data integrity, subvolumes, snapshots, rollback capability.
        
    - **Pros**: Great for backup-friendly systems and SSDs; supports multiple devices in a single volume (RAID-like).
        
    - **Cons**: Slightly higher complexity, historically had some stability concerns (mostly resolved).
        
    - **Use Case**: Home directories, servers needing snapshots, SSDs for advanced storage management.
        
- **XFS**
    
    - High-performance filesystem optimized for **large files and high-capacity storage**.
        
    - **Features**: Excellent scalability, journaling, allocation groups for fast parallel I/O.
        
    - **Pros**: Handles large files efficiently, stable for enterprise and database workloads.
        
    - **Cons**: Not ideal for small files; resizing is more complicated than ext4.
        
    - **Use Case**: Media servers, databases, large storage volumes.
        
- **F2FS (Flash-Friendly File System)**
    
    - Designed specifically for **NAND flash storage** (SSDs, eMMC).
        
    - **Features**: Log-structured design to reduce write amplification, improve lifespan of flash devices.
        
    - **Pros**: Optimized for SSD performance, low wear on flash memory.
        
    - **Cons**: Less mature, not suitable for traditional HDDs.
        
    - **Use Case**: Laptops, SSD root partitions, embedded devices.
        

---

### 🔹 Windows Filesystems

- **NTFS (New Technology File System)**
    
    - **Default** for Windows NT-based systems (Windows 2000+).
        
    - **Features**: Journaling, permissions/ACLs, compression, encryption (EFS), large file support (>16 TB).
        
    - **Pros**: Very reliable for Windows, supports advanced file attributes and security.
        
    - **Cons**: Limited cross-platform support; Linux requires `ntfs-3g` for full read/write.
        
    - **Use Case**: System partitions (`C:`), large storage volumes, Windows-only drives.
        
- **FAT32 (File Allocation Table 32-bit)**
    
    - Legacy filesystem used for cross-platform compatibility.
        
    - **Features**: Simple, supported by nearly all OSes (Linux, macOS, Windows, even cameras/USB devices).
        
    - **Pros**: Maximum compatibility.
        
    - **Cons**: Cannot store files larger than **4 GB**, partition size limited to 2 TB.
        
    - **Use Case**: USB sticks, SD cards, external drives shared across multiple OSes.
        
- **exFAT (Extended File Allocation Table)**
    
    - Designed as a modern replacement for FAT32.
        
    - **Features**: Supports very large files (>16 EB theoretical), large volumes, lightweight.
        
    - **Pros**: Excellent for external storage, compatible with Linux, macOS, and Windows.
        
    - **Cons**: No journaling, slightly less robust than NTFS.
        
    - **Use Case**: USB drives, external SSDs/HDDs shared across OSes.
        

---

### 🔹 macOS Filesystems

- **APFS (Apple File System)**
    
    - **Default** from macOS High Sierra (10.13+) onward.
        
    - **Features**: Copy-on-write, snapshots, encryption, space sharing, fast SSD performance.
        
    - **Pros**: Excellent performance on SSDs, integrated encryption (FileVault), supports cloning and snapshots.
        
    - **Cons**: Limited cross-platform support; read-only on Windows/Linux without special drivers.
        
    - **Use Case**: System drives, macOS SSDs, iOS device backups.
        
- **HFS+ (Hierarchical File System Plus)**
    
    - Older macOS filesystem (pre-APFS).
        
    - **Features**: Journaling, metadata support.
        
    - **Pros**: Stable for older systems, widely supported in macOS before 2017.
        
    - **Cons**: Less optimized for SSDs, no native snapshot or cloning support.
        
    - **Use Case**: Legacy macOS systems, older external drives.
        

---

### 🔹 Key Takeaways

- **Linux** → ext4 for most use, Btrfs/XFS for advanced or enterprise needs, F2FS for SSDs.
    
- **Windows** → NTFS for internal drives, exFAT/FAT32 for shared external storage.
    
- **macOS** → APFS for modern systems, HFS+ only for legacy.
    
- **Cross-platform drives** → exFAT is safest for sharing between Linux, Windows, and macOS.
---

## 🧠 3. Cross-Platform Considerations

- **FAT32 & exFAT** → Best for external drives shared between Linux, Windows, and macOS.  
- **NTFS** → Linux can read/write with `ntfs-3g`; Windows native.  
- **ext4** → Linux-only; requires third-party tools for Windows/macOS.  
- **APFS/HFS+** → macOS-only; Linux and Windows can read with additional drivers.

---

## 🧠 4. Partition Use Cases

- **EFI System Partition (ESP)** → FAT32, ~100–512 MB, required for UEFI boot.  
- **Root (`/`)** → ext4 (Linux), NTFS (Windows), APFS (macOS).  
- **Home/Data** → ext4, NTFS, exFAT depending on sharing needs.  
- **Swap** → Linux-only swap partition or swapfile.

---

## 💡 Notes & Tips

- For **dual-boot**, always use **GPT + UEFI** for modern systems.  
- Always align **filesystem type with OS support** to avoid data loss.  
- When encrypting volumes, Linux often uses **LUKS**; Windows uses **BitLocker**; macOS uses **FileVault**.

---

