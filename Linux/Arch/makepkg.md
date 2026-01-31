`makepkg` is a core utility in **Arch Linux** and other Arch-based distributions used for building and installing packages from source, particularly **PKGBUILD files**. It’s what AUR helpers like `yay` use under the hood. Let me break it down:

---

### **1. Purpose**

- `makepkg` **reads a `PKGBUILD` file** (a shell script with package instructions) and **builds a package**.
    
- It produces a `.pkg.tar.zst` file, which can then be installed with `pacman`.
    

---

### **2. How it works**

1. Downloads the source code or binaries specified in the PKGBUILD.
    
2. Verifies integrity using checksums or PGP keys.
    
3. Compiles the software (if needed).
    
4. Packs it into a compressed package file.
    
5. Optional: Installs it using `pacman -U`.
    

---

### **3. Common Arguments**

- `-si`: Build and install the package after building.
    
- `-s`: Automatically install any dependencies required to build.
    
- `-c`: Clean up leftover files after building.
    
- `-p <path>`: Specify a different PKGBUILD location.
    

---

### **4. How it relates to `yay`**

- `yay` is essentially a **wrapper around `makepkg`**:
    
    - It fetches PKGBUILD files from the AUR.
        
    - Runs `makepkg` to build the package.
        
    - Installs it automatically.
        

---

**In short:** `makepkg` = the Arch “package builder.” It reads instructions in a PKGBUILD, compiles/builds the software, and produces a package ready for `pacman`.