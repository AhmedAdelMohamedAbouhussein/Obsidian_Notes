### **1. Definition**

- **Global Illumination (GI)** is a rendering technique that simulates **all light interactions in a scene**, not just direct lighting.
    
- Unlike **direct illumination**, GI accounts for:
    
    - **Reflections** (light bouncing off surfaces)
        
    - **Refractions** (light passing through transparent objects)
        
    - **Diffuse inter-reflections** (light scattering off walls and objects)
        
- GI produces **photorealistic lighting** where objects affect each other’s illumination.
    

---

### **2. How Global Illumination Works**

1. **Primary Rays**
    
    - Cast from the **camera into the scene** to find intersections with objects.
        
2. **Secondary Rays**
    
    - **Reflection Rays** → simulate light bouncing off shiny surfaces
        
    - **Refraction Rays** → simulate light passing through transparent surfaces
        
    - **Shadow Rays** → check visibility of light sources for shading
        
3. **Indirect Lighting**
    
    - Light hitting one object may **bounce onto others**, contributing to their illumination.
        
    - Example: A red wall reflects red light onto nearby surfaces.
        
4. **Energy Conservation**
    
    - GI calculations maintain **energy balance**, ensuring light intensity diminishes realistically with each bounce.
        

---

### **3. Techniques to Compute GI**

|Technique|Description|
|---|---|
|**Ray Tracing / Path Tracing**|Simulate multiple ray bounces for realistic lighting; most accurate, computationally expensive|
|**Radiosity**|Calculates light transfer between diffuse surfaces using energy exchange; good for soft, realistic diffuse light|
|**Photon Mapping**|Emits photons from light sources, stores interactions in a map, then traces rays from camera; efficient for caustics and complex reflections|

---

### **4. Components of Lighting in GI**

|Component|Role|
|---|---|
|**Direct Illumination**|Light that reaches a surface directly from a source|
|**Indirect Illumination**|Light bouncing off other surfaces to reach the surface|
|**Ambient Light**|Background light present even without a direct source|
|**Specular Reflection**|Mirror-like reflections of light sources|
|**Diffuse Reflection**|Scattered light that contributes to soft shadows and color bleeding|

---

### **5. Advantages**

- Realistic **shadows, reflections, and color bleeding**
    
- Enhances **depth and realism** in CGI scenes
    
- Critical for **movies, architectural visualization, and product rendering**
    

---

### **6. Challenges**

- **High computational cost** → slow rendering for high-resolution scenes
    
- Requires **optimizations** like:
    
    - **Bounding Volume Hierarchies (BVH)** for faster ray-object intersection
        
    - **Adaptive sampling** to reduce unnecessary ray calculations
        
    - **Denoising algorithms** to smooth noisy GI results
        

---

### **7. Summary**

- Global Illumination models **all interactions of light in a scene**, including **direct and indirect lighting**.
    
- Ray tracing with GI simulates **real-world light behavior**:
    
    - Light bounces multiple times
        
    - Colors influence surrounding objects
        
    - Shadows and reflections are accurate
        
- GI is essential for **photorealistic rendering**, though computationally intensive.