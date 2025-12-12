## **2. Bash `source` Command**

**What it is:**

- `source` is a Bash built-in command that executes a script in the **current shell** rather than creating a new shell process.
    
- This is important when you want changes (like environment variables or aliases) to persist in your current shell session.
    

**Usage:**
![[Pasted image 20251212151251.png]]

Equivalent shorthand:
![[Pasted image 20251212151303.png]]

**Why it’s needed:**

- If you just run a script normally (`./my_script.sh`), it runs in a **subshell**. Any environment variable changes disappear after the script ends.
    
- With `source`, the current shell **keeps the changes**.
    

**Platform support:**

- Linux ✅
    
- macOS ✅
    
- Windows ❌ (PowerShell uses `.` differently: `. ./my_script.ps1`)