### **1. Definition of a Pixel**

- A **pixel** (picture element) is the **smallest controllable unit** of a digital image or display.
    
- Each pixel can display a **specific color and brightness**.
    
- Pixels are arranged in a **grid** to form an image.
    

---

### **2. Key Terms**

|Term|Meaning|
|---|---|
|**Resolution**|Number of pixels in width × height (e.g., 1920×1080)|
|**Color Depth**|Number of bits used to represent the color of one pixel (e.g., 8-bit, 24-bit)|
|**Frame Buffer**|Memory area where pixel values are stored before being sent to the display|
|**DPI / PPI**|Dots per inch / Pixels per inch — indicates pixel density on a display or print|

---

### **3. Calculating Total Pixels**

- Formula:
    

Total Pixels=Horizontal Resolution×Vertical Resolution\text{Total Pixels} = \text{Horizontal Resolution} \times \text{Vertical Resolution}Total Pixels=Horizontal Resolution×Vertical Resolution

- Example:
    
    - Resolution = 1920×1080
        
    - Total Pixels = 1920 × 1080 = 2,073,600 pixels (~2.07 million)
        

---

### **4. Calculating Frame Buffer Size**

- **Frame Buffer** stores color information for every pixel. Size depends on **color depth**.
    

**Formula:**

Frame Buffer Size (bits)=Total Pixels×Color Depth (bits per pixel)\text{Frame Buffer Size (bits)} = \text{Total Pixels} \times \text{Color Depth (bits per pixel)}Frame Buffer Size (bits)=Total Pixels×Color Depth (bits per pixel)

- Convert bits to bytes: 1 byte = 8 bits
    

**Example:**

- Resolution: 1920×1080 → 2,073,600 pixels
    
- Color Depth: 24-bit (8 bits per R/G/B channel)
    

Size=2,073,600×24=49,766,400 bits≈6.0 MB\text{Size} = 2,073,600 \times 24 = 49,766,400 \text{ bits} \approx 6.0 \text{ MB}Size=2,073,600×24=49,766,400 bits≈6.0 MB

---

### **5. Calculating Storage for Multiple Frames (Video)**

- Formula:
    

Video Storage (bits)=Frame Buffer Size×Number of Frames\text{Video Storage (bits)} = \text{Frame Buffer Size} \times \text{Number of Frames}Video Storage (bits)=Frame Buffer Size×Number of Frames

- For **frames per second (FPS)** video:
    

Video Storage=Frame Buffer Size×FPS×Seconds\text{Video Storage} = \text{Frame Buffer Size} \times \text{FPS} \times \text{Seconds}Video Storage=Frame Buffer Size×FPS×Seconds

**Example:**

- 1920×1080, 24-bit color, 30 FPS, 10 seconds
    

6 MB/frame×30×10=1800 MB (uncompressed)6 \text{ MB/frame} \times 30 \times 10 = 1800 \text{ MB (uncompressed)}6 MB/frame×30×10=1800 MB (uncompressed)

> **Note:** Compression (e.g., JPEG, H.264) reduces this drastically.

---

### **6. Bits per Pixel (Color Representation)**

|Color Depth|Number of Colors|Bits per Pixel|
|---|---|---|
|1-bit|2 (black/white)|1|
|8-bit|256|8|
|16-bit|65,536|16|
|24-bit|16.7 million|24|
|32-bit|16.7 million + alpha|32|

---

### **7. Pixel Pitch and Physical Size**

- **Pixel Pitch** = distance between centers of two adjacent pixels (mm)
    
- Smaller pitch → higher **pixel density** → sharper images
    
- **Formula:**
    

PPI=H2+V2Screen Diagonal (inches)\text{PPI} = \frac{\sqrt{H^2 + V^2}}{\text{Screen Diagonal (inches)}}PPI=Screen Diagonal (inches)H2+V2​​

---

### **8. Summary Formulas**

1. **Total Pixels** = Horizontal × Vertical
    
2. **Frame Buffer Size (bits)** = Total Pixels × Color Depth
    
3. **Frame Buffer Size (bytes)** = Frame Buffer Size (bits) ÷ 8
    
4. **Video Storage (bits)** = Frame Buffer × FPS × Duration
    
5. **Pixel Density (PPI)** = √(H² + V²) ÷ Diagonal