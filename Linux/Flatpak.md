## 1️⃣ Introduction

**Flatpak** is a **universal Linux application packaging and distribution system**.  
It allows developers to **package applications with all their dependencies** in a single bundle, so apps can run **across multiple Linux distributions** without modification.

- Created to solve dependency hell on Linux
- Works on **any modern Linux distribution**
- Focused on **sandboxed, secure applications**

---

## 2️⃣ Key Concepts

1. **Sandboxing**
    
    - Each Flatpak app runs in an **isolated environment**, limiting access to the host system.
    - Ensures **security and stability**.
        
2. **Runtimes**
    
    - Flatpak apps rely on **runtimes**, which provide **common libraries and dependencies**
    - Example: GNOME runtime, KDE runtime.
    - Apps can share runtimes, saving space.
    
3. **Bundles**
    
    - A Flatpak app contains:
        
        - The application itself
        - Its dependencies (if not in runtime)
        - Metadata (permissions, sandbox rules)
            
4. **Repositories (Remotes)**
    
    - Flatpak uses **remotes** to fetch apps.
    - Popular remote: **Flathub** (main Flatpak app repository)
    - Users can add multiple remotes.

---

## 3️⃣ Flatpak Architecture

![[Pasted image 20251218171619.png]]

- **Host system** provides kernel and basic OS features
- **Runtime** provides libraries (shared across apps)
- **Sandbox** isolates apps from the system

---

## 4️⃣ Installation & Usage

### 4.1 Installing Flatpak

`# Arch Linux sudo pacman -S flatpak  # Ubuntu/Debian sudo apt install flatpak`

### 4.2 Adding a Remote

`# Add Flathub repository flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`

### 4.3 Installing an App

`flatpak install flathub com.spotify.Client`

### 4.4 Running an App

`flatpak run com.spotify.Client`

### 4.5 Updating Apps

`flatpak update`

### 4.6 Listing Installed Apps

`flatpak list`

---

## 5️⃣ Permissions & Sandboxing

- Flatpak apps **do not have full access** to the host system by default
- Permissions can be managed using:

`flatpak info --show-permissions com.spotify.Client flatpak override --filesystem=home com.spotify.Client`

- Examples of permissions:
    
    - Filesystem access
    - Network access
    - Hardware (camera, microphone)

---

## 6️⃣ Advantages of Flatpak

1. **Cross-distro compatibility** → works on Fedora, Ubuntu, Arch, etc.
2. **Sandboxing** → improves security
3. **Dependency management** → apps bring libraries they need
4. **Easier updates** → runtime and apps updated independently
5. **User installs** → does not require root for installation

---

## 7️⃣ Disadvantages

- Larger app size (due to bundled dependencies)
- Uses disk space for runtimes
- Slightly slower startup compared to native apps

---

## 8️⃣ Flatpak vs Snap vs AppImage

|Feature|Flatpak|Snap|AppImage|
|---|---|---|---|
|Sandboxed|Yes|Yes|Optional|
|Cross-distro|Yes|Yes|Yes|
|Requires Daemon|Yes|Yes|No|
|Updates|Manual/Auto|Auto|Manual|
|App Size|Medium|Large|Small|

---

## 9️⃣ Summary

- **Flatpak** is a **universal, sandboxed package system for Linux**
- Runs apps **isolated from the host system**
- Uses **runtimes** for shared dependencies
- Apps are installed and updated via **remotes** like Flathub
- Good for **cross-distro apps, security, and version consistency**