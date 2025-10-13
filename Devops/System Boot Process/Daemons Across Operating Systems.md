## 🧩 **Daemons Across Operating Systems**

### 🐧 **Linux / Unix**

- Uses **daemons** — background processes managed by **systemd** (or older init systems).
    
- Examples:
    
    - `sshd` → Secure Shell service
        
    - `NetworkManager` → Handles Wi-Fi
        
    - `cupsd` → Printing service
        

🧰 Managed with:

`systemctl start <daemon> systemctl enable <daemon> systemctl status <daemon>`

---

### 🪟 **Windows**

- Equivalent concept: **Windows Services**
    
- These are background processes that start at boot and run without a user session.
    

💡 Examples:

- `Spooler` → Handles printer jobs
    
- `wuauserv` → Windows Update
    
- `WinDefend` → Windows Defender antivirus
    

🧰 Managed with:

- **GUI**: `services.msc`
    
- **Command Line (PowerShell):**
    
    `Get-Service Start-Service -Name "Spooler" Stop-Service -Name "Spooler" Set-Service -Name "Spooler" -StartupType Automatic`
    

🧠 In short:

> Windows _services_ = Linux _daemons_

---

### 🍎 **macOS**

- macOS also has **daemons**, but they are managed by the **launchd** system.
    

💡 Examples:

- `com.apple.AirPlayXPCHelper` → AirPlay service
    
- `com.apple.backupd` → Time Machine backups
    

🧰 Managed with:

`launchctl list        # Show running daemons sudo launchctl start <service> sudo launchctl stop <service> sudo launchctl enable system/<service>`

macOS has:

- **LaunchDaemons** → Run system-wide (before user login)
    
- **LaunchAgents** → Run after a user logs in
    

---

### ⚖️ **Summary Table**

|OS|Name|Manager|Example|Runs When|
|---|---|---|---|---|
|**Linux**|Daemon|`systemd`|`sshd`, `preload`|System boot|
|**Windows**|Service|`services.msc`, PowerShell|`wuauserv`, `Spooler`|System boot|
|**macOS**|Daemon / Agent|`launchd`|`com.apple.backupd`|Boot / User login|

---

✅ **In short:**  
All modern operating systems use **background services** (daemons or equivalents) — they just differ in naming and management tools.