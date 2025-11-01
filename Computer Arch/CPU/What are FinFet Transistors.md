# 🧠 **FinFET Transistors**

---

### **1. Definition**

- **FinFET (Fin Field-Effect Transistor)** is a **3D transistor design** used in modern CPUs, GPUs, and SoCs.
    
- Named for its **fin-like structure**, which stands vertically on the silicon substrate.
    
- Replaces traditional **planar (2D) transistors** for better **performance and power efficiency** at small process nodes (≤22 nm).
    

---

### **2. Structure**

- **Fin** → thin vertical silicon strip that forms the **channel** where current flows.
    
- **Gate** → wraps around the fin on **three sides (tri-gate)** for better control of current.
    
- **Source and Drain** → ends of the fin where current enters and exits.
    
- **Substrate** → base layer of silicon.
![[Pasted image 20251022180339.png]]

### **3. Advantages Over Planar Transistors**

|Feature|Planar MOSFET|FinFET|
|---|---|---|
|Gate Control|Single plane|Wraps 3 sides of fin → stronger control|
|Leakage Current|Higher at small nodes|Lower → less power wasted|
|Short-Channel Effects|More pronounced|Reduced → better scalability|
|Power Efficiency|Moderate|High → lower voltage and power|
|Density|Limited|Higher → more transistors per mm²|

---

### **4. Operating Principle**

- **Gate voltage** controls current flow through the **fin channel**.
    
- Tri-gate design allows better **electrostatic control** → reduces **leakage** and allows **faster switching**.
    
- Smaller fins → **higher drive current** and **better performance**.
    

---

### **5. Applications**

- CPUs (Intel, AMD, ARM processors)
    
- GPUs and AI chips
    
- Mobile SoCs (smartphones and tablets)
    

---

### **6. Scaling**

- FinFET technology enables **process nodes down to 3–5 nm**.
    
- Smaller nodes → more transistors per chip → **higher performance and efficiency**.
    

---

### **7. Summary**

- **FinFET** = 3D transistor with a **fin-shaped channel** and **tri-gate**.
    
- Replaces planar MOSFET for **modern high-density chips**.
    
- Advantages: **lower leakage, higher speed, better power efficiency, and scalability**.