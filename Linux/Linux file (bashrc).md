**What it is:**

- A configuration file for Bash **interactive shells**.
    
- Contains settings like: environment variables, aliases, custom functions, prompts, PATH modifications, etc.
    

**Example contents:**
![[Pasted image 20251212151354.png]]

**How it works:**

- Runs automatically when a **new interactive Bash shell** opens.
    
- Use `source ~/.bashrc` to apply changes immediately.
    

**Platform support:**

- Linux ✅
    
- macOS ✅ (for Bash; macOS defaults to zsh now, but ~/.zshrc is equivalent)
    
- Windows ❌ unless using WSL or Git Bash
