# Rasterization

### Meaning

**Rasterization** is the process of **converting vector graphics or 3D objects into a grid of pixels** (a raster) that can be displayed on a screen.

- Takes geometric data (lines, shapes, triangles) → produces **pixels with colors**.
    
- Fundamental in **computer graphics, GPUs, and rendering pipelines**.
    

---

## 1. How It Works (2D Example)

- Input: vector shapes (lines, circles, polygons)
    
- Output: pixels on a screen grid
    

Example:

- A triangle defined by three vertices
    
- Rasterization fills in **all pixels inside the triangle**
    
- Colors each pixel based on:
    
    - Fill color
        
    - Texture
        
    - Lighting (in 3D)
        

---

## 2. 3D Graphics Rasterization

In **3D rendering** (games, OpenGL, DirectX, WebGL):

1. **Vertices transformed** from 3D → 2D (projection)
    
2. **Clipping**: remove parts outside the screen
    
3. **Rasterization**: convert triangles into pixels
    
4. **Shading & Texturing**: apply colors, lighting, textures
    
5. **Framebuffer**: final image displayed
    

---

## 3. Key Points

- **Rasterization vs Ray Tracing**:
    
    - Rasterization: fast, pixel-by-pixel, standard in GPUs
        
    - Ray tracing: simulates light rays, realistic, slower
        
- **Used in**:
    
    - Video games
        
    - GUI rendering
        
    - Web browsers (canvas, WebGL)
        
- Hardware acceleration via **GPU pipelines**
    

---

## 4. Memory Hook

- Think: **“Vector → Pixels”**
    
- Vector = math shapes
    
- Raster = screen grid
    
- Rasterization = **painting pixels from shapes**
    

---

## 5. One-Line Exam Answer

> Rasterization is the process of converting geometric shapes or 3D objects into a grid of pixels for display on a screen.