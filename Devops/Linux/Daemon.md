## 🧩 **What is a Daemon in Linux?**

A **daemon** (pronounced **DEE-muhn**) is a **background process** that runs quietly without direct user interaction.  
It often starts automatically at boot and continues running to provide essential services.

---

### 🧠 **In Simple Terms**

A daemon is like an **invisible helper** that:

- ⚙️ Starts when your system boots (before you log in)
    
- 🏃‍♂️ Keeps running in the background
    
- 💬 Waits for requests or performs system tasks automatically
    

---

### 💡 **Common Examples of Daemons**

|🧩 Daemon|📝 Description|
|---|---|
|`preload`|Speeds up app launch times by caching frequently used programs|
|`sshd`|Handles SSH connections (remote access to your system)|
|`NetworkManager`|Manages Wi-Fi and Ethernet network connections|
|`cupsd`|Manages printers and print jobs|
|`swww-daemon`|Handles wallpaper transitions and animations in Hyprland|

---

### ⚙️ **Controlling Daemons with `systemctl`**

You can use the `systemctl` command (part of **systemd**) to manage daemons:

`# Start a daemon sudo systemctl start preload  # Stop a daemon sudo systemctl stop preload  # Enable it to start on boot sudo systemctl enable preload  # Check if it’s running systemctl status preload`

🧠 **Pro tip:**  
Daemons are usually stored as `.service` files inside `/etc/systemd/system/` or `/usr/lib/systemd/system/`.

---

### 🧩 **In Short**

> **Daemon = a background service** that performs system tasks automatically,  
> ensuring your Linux system runs smoothly without manual intervention.