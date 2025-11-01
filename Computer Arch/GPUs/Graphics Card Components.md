## 🧩 **1. Overview**

A **graphics card (GPU)** is a dedicated hardware component designed to handle image rendering, video output, and parallel computations.  
It combines **electronic circuits, memory, cooling, and connectors** on a single printed circuit board (PCB).

### 🧠 In short:

> A GPU = **processor + memory + power + cooling + output interfaces**, all working together to generate frames and send them to your display.

---

## 🧱 **2. Main Components**

### **1️⃣ GPU Chip (Graphics Processing Unit)**

- The **core brain** of the graphics card — often referred to as the **die** (e.g., _GA102, AD102_).
    
- Performs all the rendering, shading, and compute operations.
    
- Made up of:
    
    - **Streaming Multiprocessors (SMs)** → contain CUDA cores, Tensor cores, RT cores
        
    - **Texture units & ROPs** → handle image textures and final pixel output
        
    - **Cache hierarchy** → L1, L2, etc. for faster access
        

🧠 **Analogy:** GPU chip = the CPU of the graphics card.

---

### **2️⃣ VRAM (Video Random Access Memory)**

- High-speed memory used by the GPU to **store textures, frame buffers, and compute data**.
    
- Modern GPUs use **GDDR6 or GDDR6X** memory chips.
    
- Connected to the GPU through a **memory bus** (e.g., 256-bit, 384-bit).
    

|Feature|Description|
|---|---|
|**Type**|GDDR5 / GDDR6 / GDDR6X / HBM2e|
|**Purpose**|Store frames, textures, shaders, compute buffers|
|**Speed**|Extremely fast (up to 1 TB/s bandwidth)|

🧠 More VRAM = better handling of large textures, higher resolutions, and multitasking.

---

### **3️⃣ VRM (Voltage Regulation Module)**

- Controls and stabilizes **power delivery** to the GPU and memory.
    
- Converts **12V from PSU** → fine-tuned voltages (like 1.0V or lower) for GPU core and memory.
    
- Consists of:
    
    - **MOSFETs**
        
    - **Chokes (inductors)**
        
    - **Capacitors**
        
    - **Power phases**
        

🧠 More VRM phases = more stable power → better overclocking and cooling.

---

### **4️⃣ Cooling System**

Keeps the GPU and VRAM within safe temperature limits.

Types:

|Cooling Type|Description|
|---|---|
|**Air cooling**|Fans + heatsinks (most common)|
|**Blower style**|Single fan pushes air out the back (used in compact builds)|
|**Liquid cooling**|Uses water blocks and radiators (used in high-end GPUs)|

Components:

- **Fans** → move air
    
- **Heatsink** → absorbs heat
    
- **Thermal paste/pads** → transfer heat from GPU/VRAM to heatsink
    

---

### **5️⃣ PCB (Printed Circuit Board)**

- The main board that connects **all components**: GPU, VRAM, VRM, sensors, and connectors.
    
- Carries **power delivery traces**, **signal lines**, and **data buses**.
    

🧠 The quality of PCB design affects performance, overclocking, and heat distribution.

---

### **6️⃣ Power Connectors**

- Supply additional power beyond the PCIe slot’s 75W limit.
    

|Connector|Power (approx)|
|---|---|
|6-pin PCIe|75 W|
|8-pin PCIe|150 W|
|12VHPWR (new standard)|up to 600 W|

🧠 Example: RTX 4090 can draw 450W+, requiring a 12VHPWR connector.

---

### **7️⃣ Display Output Ports**

Used to connect your monitor(s).

|Port|Description|
|---|---|
|**HDMI**|Common for TVs and monitors|
|**DisplayPort**|High refresh rate & resolution (up to 8K)|
|**DVI**|Older digital connection|
|**VGA**|Legacy analog connection|

🧠 Modern GPUs typically have **3× DisplayPort + 1× HDMI**.

---

### **8️⃣ BIOS Chip**

- Stores the GPU’s firmware, fan curves, and voltage/frequency tables.
    
- Controls initialization during system boot.
    

🧠 Enthusiasts sometimes **flash modified BIOSes** for better overclocking (risky).

---

### **9️⃣ PCI Express Interface**

- The connector that slots into your motherboard.
    
- Modern GPUs use **PCIe 4.0 ×16** or **PCIe 5.0 ×16** for high bandwidth.
    
- Backward-compatible with older PCIe versions.
    

🧠 Acts as the **data bridge** between the GPU and CPU/system memory.

---

### **🔟 Backplate (Optional)**

- Metal or composite plate mounted on the rear of the card.
    
- Adds structural support, cooling, and aesthetic appeal.
    

🧠 Some backplates are active (with heat pads), others purely cosmetic.

---

## ⚙️ **3. Internal Data Flow**

Here’s how data moves through a GPU during rendering:

`CPU → PCIe Bus → GPU → VRAM → Shader Units → Render Output Units (ROPs) → Display Output (HDMI/DP)`

1. **CPU** sends draw calls and data.
    
2. **GPU** processes geometry, shading, lighting.
    
3. **VRAM** stores temporary data (textures, frame buffers).
    
4. **ROPs** finalize pixels and send the frame to the monitor.
    

---

## 💡 **4. Example: NVIDIA RTX 4090 (AD102)**

|Component|Specification|
|---|---|
|**GPU Die**|AD102 (Ada Lovelace)|
|**CUDA Cores**|16,384|
|**VRAM**|24 GB GDDR6X|
|**Memory Bus**|384-bit|
|**VRM**|20-phase|
|**Power Draw**|~450 W|
|**PCIe Interface**|PCIe 4.0 ×16|
|**Cooling**|Triple-fan + vapor chamber|

---

## 🧠 **5. Summary Table**

|Component|Function|
|---|---|
|**GPU Chip**|Core processor that handles graphics computations|
|**VRAM**|High-speed memory for textures and frames|
|**VRM**|Power management and regulation|
|**Cooling System**|Keeps temperature stable|
|**PCB**|Circuit backbone connecting all parts|
|**Power Connectors**|Deliver extra energy|
|**Ports**|Connect displays|
|**BIOS**|Stores firmware|
|**PCIe Interface**|Connects GPU to motherboard|
|**Backplate**|Adds strength and helps cooling|