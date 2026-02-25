## 1️⃣ Definition

**WinSCP** is a **free Windows application** for **file transfer and remote file management**.

- Supports **SFTP, SCP, FTP, FTPS, and WebDAV** protocols
    
- Provides both a **graphical interface (GUI)** and **command-line scripting**
    
- Primarily used to **securely transfer files between local and remote computers**
    

---

## 2️⃣ Key Features

|Feature|Description|
|---|---|
|Protocol support|SFTP, SCP (over SSH), FTP, FTPS, WebDAV|
|GUI interfaces|**Explorer-style** and **Commander-style**|
|Drag-and-drop|Easy transfer between local & remote|
|Synchronization|Directory comparison and sync|
|Scripting / Automation|Supports **batch scripts** and **command-line automation**|
|Integration|Can work with **PuTTY/SSH** for terminal sessions|
|Encryption|Uses SSH / SSL for secure transfers|
|Session management|Save multiple remote server sessions|

---

## 3️⃣ Common Use Cases

1. **Upload / Download files** to/from a server (web server, cloud, or VPS)
    
2. **Remote file editing** without downloading files manually
    
3. **Synchronize directories** between local and remote systems
    
4. **Automate backups** using WinSCP scripting
    

---

## 4️⃣ Installation & Setup

1. Download from [https://winscp.net](https://winscp.net)
    
2. Install on Windows
    
3. Configure **new session**:
    
    - Host name / IP
        
    - Protocol (SFTP recommended)
        
    - Port (default SFTP = 22)
        
    - Username & password / private key
        
4. Save session for future use
    

---

## 5️⃣ GUI Overview

### Explorer-style:

- Left panel → **local system**
    
- Right panel → **remote system**
    
- Drag and drop files to transfer
    

### Commander-style:

- Dual-panel layout
    
- Allows **more advanced file operations**
    

---

## 6️⃣ Scripting / Command-Line Example

**Example: Upload a file automatically**

"C:\Program Files (x86)\WinSCP\WinSCP.com" /command ^  
    "open sftp://username:password@host/" ^  
    "put C:\local\file.txt /remote/path/" ^  
    "exit"

- `WinSCP.com` → command-line interface
    
- `open` → connect to server
    
- `put` → upload files
    
- `exit` → close session
    

---

## 7️⃣ Synchronization Example

- Compare local folder with remote folder
    
- Sync changes **one-way** (upload only) or **two-way**
    
- Can run **scheduled tasks** using command-line scripts
    

---

## 8️⃣ Security Features

- Supports **SSH keys** for authentication
    
- Can **store sessions with encrypted passwords**
    
- Uses **SFTP/SCP for secure transfers** instead of plain FTP
    

---

## 9️⃣ Advantages

- Free and lightweight
    
- Easy to use GUI for non-technical users
    
- Secure file transfers (SFTP/SCP)
    
- Automation through scripting for repetitive tasks
    
- Integrated with **PuTTY** for SSH terminal sessions
    

---

## 🔟 Limitations

- Windows-only (no official Linux version)
    
- GUI can be confusing for very large directories
    
- Advanced automation may require learning WinSCP scripting
    

---

## 10️⃣ Key Exam / Interview Points

- **WinSCP = Windows tool for secure file transfer**
    
- Supports **SFTP, SCP, FTP, FTPS, WebDAV**
    
- Can be used **manually (GUI)** or **automated (scripts)**
    
- Provides **file synchronization and remote editing**
    
- Works well with **SSH keys for secure authentication**