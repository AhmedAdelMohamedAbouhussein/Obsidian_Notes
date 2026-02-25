# 1️⃣ Definition

`pkg` is a **wrapper around APT** used in **Termux (Android terminal emulator)**.

- It simplifies package management commands
    
- Internally uses `apt`
    
- Designed to be beginner-friendly
    

So:

> `pkg` = simplified interface for APT in Termux

---

# 2️⃣ Where It Is Used

- Android devices running **Termux**
    
- Lightweight Linux environment inside Android
    
- Often used for:
    
    - Ethical hacking tools
        
    - Development (Python, Node.js, Git)
        
    - Linux practice on phone
        

---

# 3️⃣ Basic Commands

### Update package list

pkg update

Equivalent to:

apt update

---

### Upgrade installed packages

pkg upgrade

---

### Install a package

pkg install nmap

---

### Remove a package

pkg uninstall nmap

---

### Search for a package

pkg search python

---

# 4️⃣ What Happens Internally?

When you run:

pkg install git

Termux actually executes:

apt install git

But `pkg`:

- Automatically handles confirmations
    
- Uses recommended options
    
- Simplifies syntax
    

---

# 5️⃣ Why Use pkg Instead of apt in Termux?

|Feature|pkg|apt|
|---|---|---|
|Simpler syntax|✅|❌|
|Beginner friendly|✅|❌|
|Direct control|❌|✅|
|Used in servers|❌|✅|

For Android → use `pkg`  
For Linux servers → use `apt`

---

# 6️⃣ Example Workflow in Termux

pkg update  
pkg upgrade  
pkg install git  
pkg install python  
pkg install nmap

Now you have:

- Git
    
- Python
    
- Nmap
    

Running inside Android.

---

# 7️⃣ Differences Between pkg (Termux) and APT (Linux)

|Aspect|pkg|apt|
|---|---|---|
|Platform|Android (Termux)|Debian/Ubuntu|
|Repositories|Termux repo|Debian/Ubuntu repos|
|Root required|❌|Usually yes|
|Purpose|Lightweight mobile Linux|Full OS package manager|

---

# 8️⃣ Common Beginner Mistake

Trying to use:

pkg

On a normal Linux system like Ubuntu.

It will fail because `pkg` only exists in **Termux**.

---

# 9️⃣ Security Notes

Termux packages:

- Are built specifically for Android architecture (ARM)
    
- Use safe repositories
    
- Do not require root
    

---

# 🔟 Interview / Exam Key Points

- `pkg` = Termux package manager
    
- Wrapper around `apt`
    
- Used on Android
    
- Simplifies install/update/remove commands
    
- Not used in normal Linux distributions