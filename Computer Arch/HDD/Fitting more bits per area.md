### 🧠 **Topic: Fitting More Bits per Area (Data Density in HDDs)**

#### **1. Definition**

- “Fitting more bits per area” means **increasing the data density** on the magnetic surface of a hard disk platter.
    
- The goal is to **store more data in the same physical space** without increasing the platter size.
    

---

#### **2. Key Concepts**

- **Areal Density** = Number of bits stored per square inch on the platter.
    
    Areal Density=Track Density×Linear Bit Density\text{Areal Density} = \text{Track Density} \times \text{Linear Bit Density}Areal Density=Track Density×Linear Bit Density
    - **Track Density:** Number of tracks per inch (TPI).
        
    - **Linear Bit Density:** Number of bits per inch along a track (BPI).
        

---

#### **3. Techniques Used to Increase Bit Density**

1. **Smaller Magnetic Domains**
    
    - Each bit is represented by a magnetic domain.
        
    - By reducing domain size, more bits fit into the same area.
        
    - Requires advanced materials with **stable magnetization** to avoid bit flipping.
        
2. **Improved Read/Write Heads**
    
    - **GMR (Giant Magnetoresistance)** and **TMR (Tunneling Magnetoresistance)** heads can detect smaller magnetic changes, allowing tighter packing of bits.
        
3. **Better Error Correction Codes (ECC)**
    
    - Modern ECC algorithms allow reliable reading of data even when bits are closer together and interference increases.
        
4. **Perpendicular Magnetic Recording (PMR)**
    
    - Replaced **Longitudinal Magnetic Recording (LMR)**.
        
    - Instead of storing bits flat on the platter, PMR stores them **vertically**, which allows much higher density.
        
5. **Shingled Magnetic Recording (SMR)**
    
    - Tracks are written overlapping each other like roof shingles.
        
    - Increases areal density but reduces random write speed.
        
6. **Heat-Assisted Magnetic Recording (HAMR)**
    
    - Uses a laser to briefly heat the platter, making it easier to magnetize smaller, denser areas.
        
7. **Bit-Patterned Media (BPM)**
    
    - Each bit has its own **predefined magnetic island**, improving precision and density.
        

---

#### **4. Trade-offs**

- **Higher density** → greater risk of **magnetic interference** (bit errors).
    
- Requires **precise head positioning** and **advanced error correction**.
    
- Can reduce write speed in some methods (e.g., SMR).
    

---

#### **5. Summary**

|Method|How it Works|Advantage|Drawback|
|---|---|---|---|
|PMR|Bits stored vertically|Major density increase|Expensive to produce|
|SMR|Overlapping tracks|Higher density|Slower writes|
|HAMR|Laser-assisted writing|Extremely high density|Heat and cost issues|
|BPM|Patterned magnetic islands|Very stable storage|Complex manufacturing|