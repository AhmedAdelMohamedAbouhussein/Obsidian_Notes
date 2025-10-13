### 🔹 MBR (Master Boot Record)

- Used with **BIOS** systems.
    
- The **first 512 bytes** of the disk hold the bootloader + partition table.
    
- Supports **up to 4 primary partitions** (or 3 primary + 1 extended).
    
- **Disk size limit: 2 TB**.
    
- If the MBR is corrupted, the system may not boot.

### 🔹 GPT (GUID Partition Table)

- Used with **UEFI** systems.
    
- Stores **multiple copies** of the partition table for redundancy.
    
- Supports **128 partitions** (no need for extended ones).
    
- **Supports drives larger than 2 TB**.
    
- Includes **CRC checksums** for better reliability and error
- 
![[Pasted image 20251013225432.png]]
### 🔗 Relationship

- **BIOS** works with **MBR**.
- **UEFI** works with **GPT**.
- Some systems support **Legacy + UEFI hybrid mode**.