### 📌 `npm install react-easy-crop`

- **What it does**:  
    Installs the **`react-easy-crop`** library into your React project.
    
- **About `react-easy-crop`**:
    
    - A lightweight React component for cropping images/videos.
        
    - Commonly used for **profile pictures** (circular crops), cover photos, and any case where the user needs to zoom, pan, and crop an image.
        
    - Provides a responsive, mobile-friendly UI for cropping.
        
- **Why we use it**:
    
    - Default `<input type="file" />` only lets you select images, but **not crop them**.
        
    - With `react-easy-crop`, the user can:  
        ✅ Zoom in / out  
        ✅ Move the image inside the crop area  
        ✅ Choose circular or rectangular cropping  
        ✅ Get the cropped image area coordinates
        
- **How to install**:

    `npm install react-easy-crop`

- **How to use (basic example)**:
-![[Pasted image 20250905191914.png]]
- **Output**:
    
    - Doesn’t automatically save the cropped image.
    - Instead, it gives you the **crop coordinates** → you then use a helper function (`getCroppedImg`) to generate the final cropped image (usually with `canvas`).

---

👉 In short:  
`react-easy-crop` is the **go-to React library** for letting users upload & crop profile pictures with zoom and pan support.
