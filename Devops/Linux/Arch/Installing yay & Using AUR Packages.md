
## 🧩 Step 1 — Update your system

	sudo pacman -Syu

### Explanation

- Ensures all official repositories and installed packages are **up-to-date**.
    
- Prevents conflicts when installing AUR packages.
    

---

## 🧩 Step 2 — Install build tools

`sudo pacman -S --needed base-devel git`

### Explanation

- `base-devel` includes **compilers and essential tools** like `make`, `gcc`, and `pkg-config`.
    
- `git` is required to clone AUR repositories.
    
- Only needs to be done **once** per system.
    

---

## 🧩 Step 3 — Clone and install yay

`git clone https://aur.archlinux.org/yay.git cd yay makepkg -si`

### Explanation

- Clones the official yay repository from the AUR.
    
- `makepkg -si` builds and installs yay automatically.
    
- Once installed, yay can **handle AUR packages seamlessly**.
    

---

## 🧩 Step 4 — Install Visual Studio Code via yay

`yay -S visual-studio-code-bin`

### Explanation

- `visual-studio-code-bin` is the **official Microsoft build** of VS Code.
    
- Yay will **download, build, and install** all dependencies automatically.
    
- Simplifies AUR usage compared to manual compilation.
    

---

## 🧩 Step 5 — Launch Visual Studio Code

- Command line:
    

`code`

- Or via **application launcher**: Appears as “Visual Studio Code”.
    
- Fully functional with **updates and extensions** supported.
    

---

## 💡 Notes

- Yay automates AUR package management but always **review the PKGBUILD** if installing unfamiliar software.
    
- After installing yay, you can use commands like:
    
    - `yay -S <package>` → Install packages
        
    - `yay -Ss <keyword>` → Search
        
    - `yay -R <package>` → Remove
        
    - `yay -Syu` → Update all packages (official + AUR)