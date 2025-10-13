### 🧩 What Is Preload?

**Preload** is an _adaptive readahead daemon_ for Linux systems.  
It runs silently in the background and **monitors which applications you use most often**, then **preloads their binaries and libraries into RAM**.

💡 **Result:**  
Your frequently used apps (like Brave, Firefox, or VS Code) launch much faster because part of them is already loaded into memory before you click.

---

### 🧠 How It Works

Preload behaves like a **smart predictive cache**:

1. Runs continuously as a **systemd daemon**.
    
2. Monitors application launch patterns.
    
3. Uses this data to **predict** what you’re likely to open next.
    
4. Loads parts of those programs into memory.
    

So when you launch your favorite app, the disk doesn’t need to fetch it — it’s already ready in RAM.

---

### 🧩 Installation (Arch Linux)

`sudo pacman -S preload`

If not found in your repositories, install it from the **AUR**:

`yay -S preload`

---

### ▶️ Enabling and Starting Preload

To make `preload` start automatically on boot:

`sudo systemctl enable preload sudo systemctl start preload`

Check its current status:

`systemctl status preload`

You should see something like:

`● preload.service - Adaptive readahead daemon    Loaded: loaded (/usr/lib/systemd/system/preload.service; enabled)    Active: active (running)`

---

### ⚙️ Optional Configuration

Configuration file location:

`/etc/preload.conf`

Inside, you can fine-tune behavior:

|Setting|Description|
|---|---|
|**interval**|How often preload analyzes usage data (in seconds).|
|**lowmem**|Minimum free memory before preload stops caching.|
|**sort_strategy**|Determines how apps are prioritized for preloading (by frequency, recency, etc.).|

---

### 🧩 Example Use Case

Suppose you open:

- **Brave Browser** every morning,
    
- **VS Code** multiple times a day,
    
- and **Obsidian** at night.
    

After a few days, preload learns this pattern.  
Next time you boot up, it preloads those apps automatically — making them open almost instantly.

---

### 🧠 Summary

|Feature|Description|
|---|---|
|**Type**|System Daemon (runs in background)|
|**Purpose**|Speed up app launch by caching|
|**Service Name**|`preload.service`|
|**Config File**|`/etc/preload.conf`|
|**Startup Command**|`sudo systemctl enable --now preload`|

---

✅ **In Short:**

> Preload makes your Linux system feel more responsive by using your unused RAM intelligently to cache frequently used apps.