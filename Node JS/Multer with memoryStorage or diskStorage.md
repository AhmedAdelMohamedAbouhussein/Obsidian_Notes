### 📌 What is **Multer**?

- Multer is a **Node.js middleware** that helps handle **file uploads** (e.g., images, PDFs) in Express.
    
- Normally, when you upload a file, it comes in the HTTP request as **binary data (multipart/form-data)**, which is hard to work with directly.
    
- Multer **parses** this request and gives you the file in a format you can easily use inside your backend.
    

---

### 📌 What is **storage** in Multer?

Multer needs to know **where to keep uploaded files**. You configure that using a **storage engine**.

There are two common storage options:

1. **`diskStorage`**
    
    - Saves the uploaded files directly to your server’s filesystem.
        
    - Example: saving images inside `uploads/` folder.
        
    - Not great if you’re deploying to the cloud (Heroku, Vercel, etc.) since files may disappear or not persist.
        
2. **`memoryStorage`**
    
    - Keeps the uploaded file in **RAM (as a Buffer)**, not on disk.
        
    - You can then send that buffer directly to another service (like **Cloudflare Images, AWS S3, or Google Cloud Storage**) without saving it locally.
        
    - Ideal for your case since you want to upload files straight to **Cloudflare Images**.
        

---

### 📌 Example with `memoryStorage`
![[Pasted image 20250927224040.png]]
Now when you use it in a route:
![[Pasted image 20250927224120.png]]

✅ **Summary:**

- Multer = parses incoming file uploads.
    
- `memoryStorage` = keeps files in RAM as `Buffer` → best for cloud uploads.
    
- You don’t need to save locally → just grab `req.file.buffer` and send it to Cloudflare Images API.