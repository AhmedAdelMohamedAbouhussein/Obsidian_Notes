# 🧠 **True Size of an SSD Microchip**

---

### **1. Definition**

- The **true size** of an SSD microchip refers to the **physical memory capacity of the NAND flash chip itself**, not the marketed size of the SSD.
    
- SSDs often **market larger sizes** than the actual usable memory due to **over-provisioning and system formatting**.
    

---

### **2. Components of SSD Capacity**

1. **NAND Flash Memory Cells**
    
    - Store the actual bits of data.
        
    - Capacity depends on the number of **cells, pages, blocks, and planes**.
        
2. **Over-Provisioned Area**
    
    - Extra memory reserved by the controller.
        
    - Used for **wear leveling, garbage collection, and bad block replacement**.
        
    - Typically **7–28% of total NAND**.
        
3. **Controller & Cache**
    
    - The SSD controller does not count toward user-accessible storage.
        
    - Cache (DRAM or SLC buffer) is temporary and also not part of marketed size.
        

---

### **3. Calculating True Capacity**

1. **Determine the number of bits per chip**:
    

Chip Bits=Cells per Plane×Planes per Chip×Bits per Cell (SLC/MLC/TLC/QLC)\text{Chip Bits} = \text{Cells per Plane} \times \text{Planes per Chip} \times \text{Bits per Cell (SLC/MLC/TLC/QLC)}Chip Bits=Cells per Plane×Planes per Chip×Bits per Cell (SLC/MLC/TLC/QLC)

2. **Convert bits to bytes**:
    

Chip Bytes=Chip Bits8\text{Chip Bytes} = \frac{\text{Chip Bits}}{8}Chip Bytes=8Chip Bits​

3. **Adjust for over-provisioning**:
    

Usable Capacity=Chip Bytes×(1−Over-Provisioning Fraction)\text{Usable Capacity} = \text{Chip Bytes} \times (1 - \text{Over-Provisioning Fraction})Usable Capacity=Chip Bytes×(1−Over-Provisioning Fraction)

**Example:**

- Chip = 2 planes, 1024 blocks per plane, 256 pages per block, 16 KB per page, TLC (3 bits/cell)
    
- Total bits = 2 × 1024 × 256 × 16 KB × 8 bits/byte × 3 bits/cell
    
- Convert to bytes → total NAND capacity
    
- Subtract 10% over-provisioning → **true usable size**
    

---

### **4. Why SSDs Advertise Larger Sizes**

- Manufacturers use **decimal GB (1 GB = 1,000,000,000 bytes)**
    
- Computers calculate **binary GB (1 GiB = 1,073,741,824 bytes)**
    
- Example: SSD advertised as 512 GB → actually ~476 GiB usable
    

---

### **5. Key Points**

|Term|Description|
|---|---|
|**NAND Capacity**|Physical memory in microchips|
|**Usable Capacity**|After over-provisioning and system formatting|
|**Over-Provisioning**|Reserved memory for endurance & performance|
|**Marketing vs True Size**|Marketing uses decimal GB; true usable size uses binary GiB|

---

### **6. Summary**

- The **true size of an SSD microchip** = actual memory stored in the NAND cells.
    
- **User-accessible capacity** is less due to:
    
    1. Over-provisioning
        
    2. File system formatting
        
    3. Binary vs decimal conversion