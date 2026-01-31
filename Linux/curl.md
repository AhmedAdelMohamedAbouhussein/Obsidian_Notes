**Definition:**  
`curl` (Client URL) is a command-line tool used to **transfer data to or from a server** using various protocols such as HTTP, HTTPS, FTP, SFTP, SCP, and more. It is widely used for downloading files, making API requests, or sending data over the internet from the terminal.

---

### **Basic Features**

1. **Download a file:**
![[Pasted image 20251213003708.png]]
- `-O` saves the file with its original name.

2. **Download and rename a file:**
![[Pasted image 20251213003735.png]]
- `-o` specifies a custom filename.

3. **Fetch the content of a webpage:**
![[Pasted image 20251213003852.png]]
- Outputs HTML content directly to the terminal.

4. **Send GET or POST requests:**
![[Pasted image 20251213003906.png]]
- `-X` specifies HTTP method.
- `-d` sends data in POST requests.

1. **Use headers or authentication:**
![[Pasted image 20251213003917.png]]
- `-H` adds HTTP headers.

1. **Follow redirects:**
![[Pasted image 20251213003929.png]]
- `-L` follows redirects automatically.

---

### **Why it’s useful**

- Fetch web content quickly from the terminal.
    
- Automate downloading files or interacting with APIs.
    
- Supports many protocols, SSL, and authentication.
    
- Works in scripts for automation.