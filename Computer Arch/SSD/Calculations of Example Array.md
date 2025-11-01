# 🧠 **Calculations of Example Memory Array**

Memory arrays (like SSD or NAND flash) are made of **cells, pages, blocks, and planes**. Calculating their **capacity, size, and layout** helps understand how storage is structured.

---

### **1. Basic Definitions**

|Term|Meaning|
|---|---|
|**Cell**|Smallest memory unit storing 1 bit (SLC) or multiple bits (MLC/TLC/QLC).|
|**Page**|Smallest read/write unit (e.g., 4 KB – 16 KB).|
|**Block**|Smallest erase unit; consists of many pages (e.g., 128–256 pages per block).|
|**Plane / Die**|Collection of blocks. Multiple planes/dies can exist in one NAND chip.|

---

### **2. Step-by-Step Calculations**

#### **Step 1 – Number of Bits in a Page**

Page Bits=Page Size (bytes)×8\text{Page Bits} = \text{Page Size (bytes)} \times 8Page Bits=Page Size (bytes)×8

**Example:**

- Page Size = 16 KB
    
- Page Bits = 16 × 1024 × 8 = **131,072 bits per page**
    

---

#### **Step 2 – Number of Bits in a Block**

Block Bits=Page Bits×Pages per Block\text{Block Bits} = \text{Page Bits} \times \text{Pages per Block}Block Bits=Page Bits×Pages per Block

**Example:**

- Pages per Block = 256
    
- Block Bits = 131,072 × 256 = **33,554,432 bits** (~4 MB per block)
    

---

#### **Step 3 – Number of Bits in a Plane**

Plane Bits=Block Bits×Blocks per Plane\text{Plane Bits} = \text{Block Bits} \times \text{Blocks per Plane}Plane Bits=Block Bits×Blocks per Plane

**Example:**

- Blocks per Plane = 1024
    
- Plane Bits = 33,554,432 × 1024 = 34,359,738,368 bits (~4 GB per plane)
    

---

#### **Step 4 – Number of Bits in a Die / Chip**

Chip Bits=Plane Bits×Number of Planes per Chip\text{Chip Bits} = \text{Plane Bits} \times \text{Number of Planes per Chip}Chip Bits=Plane Bits×Number of Planes per Chip

**Example:**

- Planes per Chip = 2
    
- Chip Bits = 34,359,738,368 × 2 = 68,719,476,736 bits (~8 GB per chip)
    

---

### **3. Bits vs Bytes**

- 1 byte = 8 bits
    
- To convert bits to bytes:
    

Bytes=Bits8\text{Bytes} = \frac{\text{Bits}}{8}Bytes=8Bits​

**Example:**

- 68,719,476,736 bits ÷ 8 = 8,589,934,592 bytes ≈ 8 GB
    

---

### **4. Including Multi-Level Cells**

- If each cell stores multiple bits:
    

Capacity (bits)=Number of Cells×Bits per Cell\text{Capacity (bits)} = \text{Number of Cells} \times \text{Bits per Cell}Capacity (bits)=Number of Cells×Bits per Cell

**Example:**

- 2 bits per cell (MLC) → doubles the storage
    
- 131,072 bits/page × 2 = 262,144 bits/page
    

---

### **5. Summary Formula**

![[Pasted image 20251022175903.png]]

### **6. Notes**

- This method can be used for **2D or 3D NAND**.
    
- 3D NAND introduces **vertical stacking**, which increases number of cells per chip without increasing the footprint.
    
- Calculations help in **designing SSD capacity, layout, and estimating performance**.