# 🧠 **Single Memory Cell**

---

### **1. Definition**

- A **memory cell** is the **smallest unit of memory** that can **store one bit of information** (`0` or `1`).
    
- It is the fundamental building block of **RAM, Flash, and other memory devices**.
    

---

### **2. Basic Structure**

- A single memory cell typically has:
    
    1. **Storage element** → stores the bit (`0` or `1`)
        
        - Could be a **capacitor** (DRAM), **flip-flop circuit** (SRAM), or **floating gate transistor** (Flash).
            
    2. **Access device** → allows the cell to be **read from or written to**
        
        - Usually a **transistor** that acts as a switch controlled by the word line.
            

---

### **3. Types of Single Memory Cells**

| Type                   | Storage Element             | Access Method                  | Notes                                     |
| ---------------------- | --------------------------- | ------------------------------ | ----------------------------------------- |
| **SRAM (Static RAM)**  | Flip-flop (4–6 transistors) | Direct access via word line    | Fast, volatile, no refresh needed         |
| **DRAM (Dynamic RAM)** | Capacitor (stores charge)   | Transistor (access transistor) | Slower than SRAM, volatile, needs refresh |
| **Flash / SSD Cell**   | Floating-gate transistor    | Voltage pulses                 | Non-volatile, stores electrons as charge  |

---

### **4. Reading a Single Cell**

- **SRAM:** Sense the voltage on the flip-flop → outputs `0` or `1`.
    
- **DRAM:** Sense the charge in the capacitor → weak signal amplified → output.
    
- **Flash:** Detect threshold voltage of floating-gate transistor → logic state.
    

---

### **5. Writing to a Single Cell**

- **SRAM:** Apply voltage to flip-flop to set `0` or `1`.
    
- **DRAM:** Charge or discharge the capacitor to store `1` or `0`.
    
- **Flash:** Apply voltage pulse to trap or remove electrons from floating gate.
    

---

### **6. Key Parameters of a Memory Cell**

|Parameter|Meaning|
|---|---|
|**Bit storage**|Stores 1 bit per cell (some Flash stores multiple bits, e.g., MLC/TLC)|
|**Access speed**|Time to read or write the cell|
|**Volatility**|Does it lose data when power is off?|
|**Endurance**|Number of write/erase cycles before failure (important for Flash)|
|**Size**|Physical area of the cell — smaller cells → higher memory density|

---

### **7. Memory Array**

- Memory cells are organized in a **grid (rows × columns)**:
    
    - **Word line** → selects the row.
        
    - **Bit line** → carries data to/from the column.
        
- A single memory cell is the **intersection of a word line and a bit line**.
    

---

### **8. Summary**

- A single memory cell stores **1 bit**.
    
- Made of **storage element + access device**.
    
- Types vary by technology: SRAM, DRAM, Flash.
    
- Cells are arranged in **arrays** for building larger memory modules.