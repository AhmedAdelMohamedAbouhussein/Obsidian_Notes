# 🧠 **How CGI (Computer-Generated Images) Work**

---

### **1. Definition**

- **CGI** refers to images and animations created **entirely by computers** rather than captured with a camera.
    
- Widely used in **movies, video games, simulations, virtual reality, and advertisements**.
    

---

### **2. Core Process**

Creating a CGI image involves **three main stages**:

---

#### **Step 1 – Modeling**

- Create **3D objects** (characters, environments, props) using software like **Blender, Maya, or 3ds Max**.
    
- Objects are built using:
    
    - **Vertices**: points in 3D space
        
    - **Edges**: lines connecting vertices
        
    - **Faces**: surfaces defined by edges (polygons, usually triangles or quads)
        
- The complete mesh forms the **3D model**.
    

---

#### **Step 2 – Texturing and Materials**

- Apply **textures** (images or procedural patterns) to give objects **color, patterns, and surface details**.
    
- Define **materials** to simulate real-world properties:
    
    - **Diffuse** → base color reflection
        
    - **Specular / Reflection** → shiny or metallic surfaces
        
    - **Transparency / Refraction** → glass or water effects
        
    - **Bump / Normal Maps** → simulate surface detail without extra geometry
        

---

#### **Step 3 – Lighting**

- Add **virtual light sources** to the scene:
    
    - **Point Lights**: single location, radiates in all directions
        
    - **Directional Lights**: simulates sunlight, parallel rays
        
    - **Spotlights**: cone-shaped illumination
        
    - **Area Lights**: large surfaces emitting light for soft shadows
        
- Light interacts with materials using **shading models** (e.g., Phong, PBR – Physically-Based Rendering).
    

---

#### **Step 4 – Camera and Perspective**

- Place a **virtual camera** to determine **viewpoint, framing, and perspective**.
    
- Set camera parameters like **focal length, field of view, and depth of field**.
    

---

#### **Step 5 – Rendering**

- Rendering converts the **3D scene into a 2D image** by simulating light and material interaction.
    
- Methods include:
    
    1. **Rasterization**: fast, used in games; converts polygons into pixels on the screen.
        
    2. **Ray Tracing**: simulates light rays bouncing in the scene for realistic lighting, shadows, reflections, and refractions.
        
    3. **Path Tracing**: advanced ray tracing considering multiple light bounces for photorealism.
        

---

#### **Step 6 – Post-Processing**

- Adjust the rendered image for **effects and realism**:
    
    - Motion blur
        
    - Depth of field
        
    - Color grading
        
    - Lens flares
        
    - Compositing multiple layers
        

---

### **3. Key Concepts**

|Term|Meaning|
|---|---|
|**Mesh**|Network of vertices, edges, and faces forming 3D objects|
|**Texture**|2D image mapped onto 3D surfaces for details|
|**Material**|Defines how a surface reacts to light|
|**Shader**|Algorithm that calculates color and light at each pixel|
|**Ray Tracing**|Traces light rays for realistic shadows, reflection, and refraction|
|**Rasterization**|Converts 3D geometry into pixels for real-time graphics|

---

### **4. Applications**

- Movies and animated films
    
- Video games and VR/AR
    
- Architectural visualization
    
- Simulations and scientific visualizations
    
- Advertising and product design
    

---

### **5. Summary**

- CGI works by **building 3D models → applying textures/materials → adding lights → rendering → post-processing**.
    
- **Rendering techniques** like ray tracing or rasterization determine **realism vs speed**.
    
- Modern CGI combines **physics-based lighting, advanced shading, and high-resolution textures** to create photorealistic images.