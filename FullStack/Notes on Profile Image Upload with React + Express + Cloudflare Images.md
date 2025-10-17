## **1. Frontend (React SettingsPage)**

The frontend is responsible for:

- Letting the user pick an image.
    
- Forcing them to crop it into a square (so profile pics are consistent).
    
- Sending the cropped image to the backend.
    
- Showing a preview of what the new profile image will look like.

### Workflow:

1. **User selects a file**
![[Pasted image 20250927225027.png]]
- - `URL.createObjectURL(file)` gives a **temporary browser URL** → lets you preview images locally without uploading yet.
        
    - Example: `blob:http://localhost:5173/8f91...`
        
2. **Crop the image**
    
    - Done with `react-easy-crop`.
        
    - `onCropComplete` gives the pixel coordinates of the crop area.
        
3. **Generate a cropped Blob**
![[Pasted image 20250927225045.png]]
- - `getCroppedImg` uses `<canvas>` to cut the image at the exact crop coordinates.
        
    - It returns a **Blob** (binary image data in memory).
        
4. **Send to backend**
![[Pasted image 20250927225106.png]]- - A **Blob** is wrapped in `FormData` → this makes it look like a regular uploaded file from a `<form>` in HTML.
        
    - The `Content-Type` is `multipart/form-data`, which is how browsers upload files.
        
5. **Show new preview**
![[Pasted image 20250927225214.png]]
6. - The cropped blob gets displayed instantly while waiting for Cloudflare upload confirmation.
        

---

## **2. Backend Setup (Express + Multer + MongoDB)**

The backend’s job:

- Receive the file from the frontend.
    
- Upload it to **Cloudflare Images**.
    
- Save the Cloudflare image URL to MongoDB under the user.
    

---

### **Multer (file parser middleware)**
![[Pasted image 20250927225230.png]]
- **Multer** is middleware that understands `multipart/form-data` requests.
    
- It extracts the uploaded file(s) and attaches them to `req.file` (or `req.files`).
    
- Using `memoryStorage()` means:
    
    - The file is stored in **RAM only** (not on disk).
        
    - You access it via `req.file.buffer` → raw bytes of the file.
        
    - Perfect for uploading to external services (Cloudflare, S3, etc.).
        

👉 No need to `npm install memoryStorage` — it comes inside `multer`.

---

### **Route wiring**

In `routes/settings.js`:
![[Pasted image 20250927225251.png]]
`upload.single("profileImage")` tells Multer:

- Expect a single file.
    
- The key must be `"profileImage"` (same as frontend `formData`).
    
- Store it in memory (`req.file`).

Controller: Upload to Cloudflare
![[Pasted image 20250927225352.png]]
### **Important details**

- `req.file.buffer` = the raw bytes of the image uploaded by the frontend.
    
- `form-data` package is required in Node to send multipart requests to Cloudflare:
![[Pasted image 20250927225416.png]]
**Frontend (React/browser):** `FormData` is built-in, so you **don’t need to install anything**. Your `axios` call works as-is.


Cloudflare returns:
![[Pasted image 20250927225436.png]]
`variants[0]` is a usable URL you can store in MongoDB.


## **3. Data Flow Summary**

1. **User picks file → React**  
    File object → temporary preview URL.
    
2. **User crops file → React**  
    Canvas generates a **Blob**.
    
3. **Blob wrapped in FormData → React**  
    Sent to backend via `axios.post`.
    
4. **Multer parses → Express**  
    File stored in RAM as `req.file.buffer`.
    
5. **Upload to Cloudflare → Backend**  
    Send `req.file.buffer` via `form-data` + axios.
    
6. **Cloudflare responds → Backend**  
    Returns public image URL in `variants`.
    
7. **Save to MongoDB → Backend**  
    `User.profilePicture = cfImage.variants[0]`.
    
8. **Frontend updates UI**  
    Show new cropped image instantly.