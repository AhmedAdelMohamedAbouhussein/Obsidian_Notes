# 🧩 WSL2 — Windows Subsystem for Linux 2

### ⚙️ What Is WSL?

**WSL (Windows Subsystem for Linux)** allows you to run a **full Linux environment directly inside Windows**, without needing a separate virtual machine or dual-boot setup.

- It’s designed for developers who want Linux tools (like `bash`, `apt`, `gcc`, or `vim`) while staying inside Windows.
    
- Perfect for programming, DevOps, and learning Linux on a Windows system.
    

---

### 🧠 WSL1 vs WSL2

|Feature|**WSL1**|**WSL2**|
|---|---|---|
|**Architecture**|Translation layer (runs Linux system calls on Windows kernel)|Full Linux kernel running in a lightweight virtual machine|
|**Performance**|Slower for Linux-native tools|Much faster (especially for I/O and Docker)|
|**Kernel**|No real Linux kernel|Real Linux kernel provided by Microsoft|
|**File Access**|Faster access to Windows files|Slower when accessing `/mnt/c/` but much faster for native Linux files|
|**Compatibility**|Limited (some tools didn’t work)|Full system compatibility — supports Docker, systemd, etc.|

✅ **In short:**  
**WSL2 = real Linux kernel + VM performance + Windows integration.**

---

### 🧩 Installing WSL2

Open **PowerShell as Administrator** and run:

`wsl --install`

To install a specific distro (like Ubuntu 24.04 LTS):

`wsl --install -d Ubuntu-24.04`

You can list all available distros:

`wsl --list --online`

---

### 🧩 Managing Distros

List installed distributions:

`wsl -l -v`

Sample output:

  `NAME            STATE           VERSION * Ubuntu-24.04    Running         2   docker-desktop  Stopped         2`

Enter your distro:

`wsl -d Ubuntu-24.04`

Stop it:

`wsl --terminate Ubuntu-24.04`

Set a default distro:

`wsl --setdefault Ubuntu-24.04`

Shutdown all running WSL instances:

`wsl --shutdown`

---

### 📦 File System Layout

Inside WSL2, your Linux filesystem lives in a **virtual disk file**:

`C:\Users\<YourName>\AppData\Local\Packages\<Distro>\LocalState\ext4.vhdx`

This `.vhdx` file acts like a **virtual hard drive**, containing everything (root filesystem, configs, binaries, etc).

---

### 🧠 Where WSL Fits Architecturally

WSL2 uses:

- **A lightweight utility VM** to run a **real Linux kernel**.
    
- **VHDX** for disk storage.
    
- **Plan9 protocol** to integrate files between Linux and Windows.
    

So you can:

- Access Windows files from Linux → `/mnt/c/Users/...`
    
- Access Linux files from Windows → `\\wsl$\Ubuntu-24.04\home\<user>`
    

---

### ⚡ Useful WSL Commands

|Command|Description|
|---|---|
|`wsl --update`|Updates the Linux kernel and components|
|`wsl --set-version <distro> 2`|Converts a distro to WSL2|
|`wsl --export <distro> file.tar`|Exports a distro as a backup|
|`wsl --import <name> <folder> <file.tar>`|Imports a distro manually|
|`wsl --unregister <distro>`|Deletes the distro completely|

---

### 🧩 System Updates Inside WSL

Just like a normal Linux distro:

`sudo apt update && sudo apt upgrade -y`

This updates packages inside your Ubuntu installation (not WSL itself).

---

### 🧩 Using Linux GUI Apps

WSL2 now supports **graphical Linux apps** (like `gedit`, `nautilus`, or `vscode`) natively on Windows.

Just install normally:

`sudo apt install gedit gedit &`

GUI apps appear with proper windowing using **WSLg** (Windows Subsystem for Linux GUI).

---

### 🧠 Common Use Cases

|Use Case|Benefit|
|---|---|
|Development|Run Linux tools on Windows without dual-boot|
|Web Servers|Test nginx, Apache, Node.js locally|
|Docker|Use real Linux containers inside Windows|
|Learning Linux|Safe sandbox for Linux commands and scripting|
|Cross-Platform Projects|Use same dev environment as on production servers|

---

### 🧩 Example Workflow

1. **Launch Ubuntu in WSL2**
    
    `wsl -d Ubuntu-24.04`
    
2. **Install a package**
    
    `sudo apt install neovim`
    
3. **Edit code**
    
    `nvim app.py`
    
4. **Run your app**
    
    `python3 app.py`
    
5. **Access files from Windows**
    
    `\\wsl$\Ubuntu-24.04\home\<user>\project`
    

---

### 🧩 Performance Tips

- Store Linux projects **inside Linux filesystem** (`~/project`), not in `/mnt/c/`, for better I/O.
    
- Regularly update the kernel:
    
    `wsl --update`
    
- Stop idle distros to save RAM:
    
    `wsl --shutdown`
    
- You can also configure resource limits in:
    
    `C:\Users\<YourName>\.wslconfig`
    

Example:

`[wsl2] memory=6GB processors=4 swap=2GB localhostForwarding=true`

---

### 💡 Summary

|Concept|Description|
|---|---|
|**WSL**|Run Linux on Windows without a VM|
|**WSL2**|Real Linux kernel inside a lightweight VM|
|**Kernel**|Provided and maintained by Microsoft|
|**Files**|Stored in a `.vhdx` virtual disk|
|**GUI Apps**|Fully supported with WSLg|
|**Best Use**|Development, Linux learning, automation, Docker|

---

✅ **In short:**

> WSL2 bridges the gap between Linux and Windows — letting you use both ecosystems seamlessly in one environment.