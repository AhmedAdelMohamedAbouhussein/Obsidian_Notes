## 🔹 What is the AUR?

**AUR = Arch User Repository**  

- Think of it as a **community app store** for Arch Linux.  
- Contains **user-contributed packages** that are **not in the official Arch repos**.  
- Packages in the AUR are called **PKGBUILDs** — scripts that tell Arch how to **build and install software**.

### 🧠 Overview Table

| Repository | Maintained by       | Example Packages                        | Description                          |
|------------|-------------------|----------------------------------------|--------------------------------------|
| core, extra, community | Arch Team          | firefox, nano, neovim                  | Official, tested, and supported      |
| AUR        | Community (users) | brave-bin, google-chrome, visual-studio-code-bin | Not official, community-maintained, very popular |

> If a package isn’t available via `sudo pacman -S package`, you’ll often find it in the **AUR**.

---

## 🔹 What is yay?

**yay = Yet Another Yaourt**  

- **AUR helper** that automates downloading, building, and installing AUR packages.  
- Without yay, installing AUR packages requires you to:
  1. Clone the AUR Git repository manually  
  2. Read the PKGBUILD  
  3. Run `makepkg -si`  
  4. Resolve dependencies yourself  

- With yay, it’s as simple as:

		yay -S brave-bin

- Yay handles everything **automatically and safely**.

---

## 🔹 Common yay Commands

| Command             | Description                        |
| ------------------- | ---------------------------------- |
| `yay -S <package>`  | Install from AUR or official repos |
| `yay -Ss <keyword>` | Search for packages                |
| `yay -R <package>`  | Remove a package                   |
| `yay -Sua`          | Update AUR packages                |
| `yay -Syu`          | Update everything (official + AUR) |

---

## ⚠️ Important Tips

- Always **read the PKGBUILD** before installing; it shows what the install script does:

`yay -G brave-bin cat brave-bin/PKGBUILD`

- AUR packages are **community-maintained**, so avoid unknown or untrusted sources.
    

---

## 💡 Summary

| Term     | Meaning                                     |
| -------- | ------------------------------------------- |
| AUR      | Arch User Repository (community app store)  |
| yay      | Tool that automates installing AUR packages |
| makepkg  | Command to manually build AUR packages      |
| PKGBUILD | Script that defines how to build a package  |
