## 1️⃣ Definition

**APT (Advanced Package Tool)** is a **package management system** used in **Debian-based Linux distributions** such as:

- Debian
    
- Ubuntu
    
- Kali Linux
    
- Linux Mint
    

APT is responsible for:

- Installing software
    
- Removing software
    
- Updating packages
    
- Managing dependencies
    
- Upgrading the entire system
    

It works with `.deb` packages and uses online repositories.

---

## 2️⃣ How APT Works (Architecture)

APT sits on top of lower-level tools:

- `dpkg` → installs `.deb` packages
    
- APT → handles repositories, dependencies, and downloads
    

### Workflow:

1. APT reads repository sources from:
    
    /etc/apt/sources.list  
    /etc/apt/sources.list.d/
    
2. Downloads package metadata
    
3. Resolves dependencies
    
4. Downloads required `.deb` files
    
5. Calls `dpkg` to install them
    

---

## 3️⃣ Key Concepts

### 📦 Package

Software bundled in `.deb` format.

### 📚 Repository

Online server that stores packages.

Example:

http://archive.ubuntu.com/ubuntu

### 🔗 Dependencies

Other packages required for a program to work.

APT automatically resolves these.

---

## 4️⃣ Most Important Commands

### Update Package List

sudo apt update

- Refreshes repository metadata
    
- Does NOT install anything
    

---

### Upgrade Installed Packages

sudo apt upgrade

- Upgrades installed packages to latest versions
    

---

### Full Upgrade (Dist Upgrade)

sudo apt full-upgrade

- Upgrades packages AND handles dependency changes
    
- May remove old packages if necessary
    

---

### Install a Package

sudo apt install nmap

- Installs package + dependencies
    

---

### Remove a Package

sudo apt remove nmap

- Removes package
    
- Keeps configuration files
    

---

### Remove Completely (Including Config)

sudo apt purge nmap

---

### Search for a Package

apt search nginx

---

### Show Package Info

apt show nginx

---

### List Installed Packages

apt list --installed

---

## 5️⃣ Difference Between apt, apt-get, and dpkg

|Tool|Purpose|
|---|---|
|`apt`|Modern, user-friendly CLI (recommended)|
|`apt-get`|Older, script-friendly tool|
|`dpkg`|Low-level installer for `.deb` files|

Example of dpkg:

sudo dpkg -i file.deb

- Does NOT resolve dependencies automatically
    

---

## 6️⃣ APT Configuration Files

|File|Purpose|
|---|---|
|`/etc/apt/sources.list`|Repository list|
|`/etc/apt/apt.conf`|Configuration options|
|`/var/lib/apt/lists/`|Downloaded package metadata|
|`/var/cache/apt/archives/`|Cached `.deb` packages|

---

## 7️⃣ Cleaning Cache

APT stores downloaded packages locally.

Clean cache:

sudo apt clean

Remove unused dependencies:

sudo apt autoremove

---

## 8️⃣ Security Features

- Uses **GPG keys** to verify repository authenticity
    
- Prevents installing tampered packages
    
- Secure by default with official repositories
    

---

## 9️⃣ Advantages

- Automatic dependency resolution
    
- Large software ecosystem
    
- Secure repositories
    
- Easy system-wide upgrades
    
- Works well for servers and desktops
    

---

## 🔟 Limitations

- Only for Debian-based systems
    
- Can break system if mixing incompatible repositories
    
- Large upgrades may require manual conflict resolution
    

---

## 11️⃣ Common Real-World Usage

### Installing development tools:

sudo apt install build-essential

### Installing server software:

sudo apt install nginx

### Installing security tools (Kali Linux):

sudo apt install nmap  
sudo apt install wireshark

---

## 12️⃣ Exam / Interview Key Points

- APT = Advanced Package Tool
    
- Used in Debian/Ubuntu-based systems
    
- Works with `.deb` packages
    
- Automatically resolves dependencies
    
- Uses repositories defined in `/etc/apt/sources.list`
    
- `apt update` ≠ `apt upgrade`
    
- `apt purge` removes config files
    
- `dpkg` is lower-level than APT