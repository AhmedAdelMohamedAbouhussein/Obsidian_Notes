## 1. **Definition**

**Graphics memory**, also known as **VRAM (Video Random Access Memory)**, is a specialized type of memory used by a **GPU (Graphics Processing Unit)** to **store and quickly access image, texture, and frame data** required for rendering graphics.

➡️ Think of it as the **workspace of the GPU** — it temporarily holds all the visual data needed to display what you see on the screen.

---

## 2. **Purpose of VRAM**

The GPU constantly reads and writes massive amounts of data — like textures, lighting maps, and frames — and needs **ultra-fast access** to maintain smooth performance.

### Main Functions:

- Stores **frame buffers** (the rendered image before display).
    
- Holds **textures**, **shaders**, and **3D models**.
    
- Keeps **Z-buffer / depth maps** for handling 3D geometry.
    
- Caches **anti-aliasing data**, **post-processing effects**, and **render targets**.
    

---

## 3. **Types of Graphics Memory**

|Type|Description|Example GPUs|
|---|---|---|
|**GDDR (Graphics Double Data Rate)**|Most common type of VRAM used in consumer GPUs. Focused on high bandwidth.|GDDR5, GDDR6, GDDR6X (used in NVIDIA RTX and AMD Radeon GPUs)|
|**HBM (High Bandwidth Memory)**|3D stacked memory placed close to the GPU die. Very wide bus, extremely fast. Used in high-end GPUs.|HBM2, HBM2e, HBM3 (used in AMD Vega, NVIDIA A100)|
|**DDR (Double Data Rate)**|Regular system memory; much slower, used in integrated GPUs.|DDR4, DDR5 (used by Intel UHD, AMD Radeon iGPUs)|

---

## 4. **How VRAM Works**

When rendering:

1. The **CPU sends** rendering commands to the **GPU**.
    
2. The GPU **fetches textures, geometry, and shaders** from VRAM.
    
3. It processes the data in **parallel** using thousands of cores.
    
4. The **final image (frame buffer)** is written to VRAM before being sent to the display.
    

🧠 **Key point:** The closer and faster the memory is to the GPU, the higher the performance — minimizing latency and bandwidth bottlenecks.

---

## 5. **VRAM Size and Performance**

|Resolution|Recommended VRAM|Example|
|---|---|---|
|1080p (Full HD)|4–6 GB|RTX 2060, RX 5600|
|1440p (2K)|8–10 GB|RTX 3060 Ti, RX 6700 XT|
|4K (UHD)|12–24 GB|RTX 4080, RX 7900 XTX|
|AI / ML / 3D Rendering|16–48 GB+|RTX 4090, NVIDIA A100|

📈 **Higher VRAM** = Better handling of large textures, multiple displays, ray tracing, and complex rendering scenes.

---

## 6. **Bandwidth and Bus Width**

### 🧮 Bandwidth Formula:

Memory Bandwidth=Memory Clock Speed×Bus Width×2\text{Memory Bandwidth} = \text{Memory Clock Speed} \times \text{Bus Width} \times 2Memory Bandwidth=Memory Clock Speed×Bus Width×2

- **Bus Width:** Number of bits the GPU can read/write in one cycle (128-bit, 192-bit, 256-bit, 384-bit).
    
- **Clock Speed:** How fast the memory operates.
    
- **Higher bandwidth** = faster data transfer between GPU and VRAM.
    

---

## 7. **GDDR Evolution**

|Generation|Bandwidth|Typical Use|
|---|---|---|
|GDDR3|~30–50 GB/s|Early 2000s GPUs|
|GDDR5|~100–200 GB/s|GTX 900 series|
|GDDR6|~300–600 GB/s|RTX 3000, RX 6000|
|GDDR6X|~700–1000 GB/s|RTX 3080–4090|
|HBM2e / HBM3|Up to 3 TB/s|NVIDIA A100, AMD Instinct MI300|

---

## 8. **Integrated vs Dedicated Memory**

|Type|Description|Example|
|---|---|---|
|**Dedicated GPU**|Has its own VRAM (faster, isolated from system RAM).|RTX, Radeon RX|
|**Integrated GPU (iGPU)**|Uses part of system RAM as graphics memory (slower).|Intel Iris, AMD Radeon Vega|

---

## 9. **Important Memory Concepts**

- **Frame Buffer:** Holds the final rendered image for display.
    
- **Texture Mapping:** Loads image textures into VRAM for 3D objects.
    
- **Mipmapping:** Stores multiple resolutions of textures to optimize rendering.
    
- **Anti-Aliasing Buffer:** Smooths jagged edges in graphics using additional VRAM.
    

---

## 10. **Summary Table**

|Feature|VRAM|System RAM|
|---|---|---|
|Location|On GPU|On motherboard|
|Access Speed|Very high|Moderate|
|Used for|Graphics & rendering|General system operations|
|Size|4–48 GB typically|8–64 GB typically|