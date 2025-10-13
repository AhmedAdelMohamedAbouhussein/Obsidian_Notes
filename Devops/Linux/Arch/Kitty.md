# Kitty Terminal Emulator 🐱

## 📘 Overview
**Kitty** is a **GPU-accelerated terminal emulator** for Linux (and macOS).  
It allows you to run shell commands like other terminals but offers **faster rendering** and **advanced features**.

---

## 🔹 Why Use Kitty?

- **Speed** 🚀  
  - Uses GPU for text rendering → smooth scrolling, faster display.  
- **Customization** 🎨  
  - Themes, fonts, transparency, and layouts can all be configured.  
- **Advanced Features** 🧩  
  - Multiple **tabs** and **window splits** in a single terminal window.  
  - Full **Unicode and emoji support**.  
  - Configurable **keybindings**.  

---

## 🔹 Alternatives

Kitty is an alternative to:

| Terminal          | Notes                        |
|------------------|------------------------------|
| gnome-terminal    | Default in GNOME             |
| konsole           | Default in KDE               |
| alacritty         | GPU-accelerated, minimal     |
| xfce4-terminal    | Default in XFCE              |

> Kitty stands out for **GPU acceleration** and advanced **layout features**.

---

## 🔹 Configuration

- Config file location:
	~/.config/kitty/kitty.conf


- You can customize:
  - Fonts (`font_family`, `bold_font`, etc.)  
  - Colors (`color_scheme`)  
  - Transparency  
  - Keybindings for tabs, splits, and navigation  

---

## 🔹 Key Features Summary

- Tabs and splits inside one window  
- GPU-accelerated text rendering → smooth scrolling  
- Supports **Unicode**, emojis, ligatures  
- Highly customizable via `kitty.conf`  
- Works on Linux and macOS  

---

## 🔹 Installation (Arch Linux)
	sudo pacman -S kitty

Or via AUR for the latest version:

`yay -S kitty-git`

---

## 💡 Notes

- Great for **power users** who want speed and flexibility.
    
- Perfect for setups like **tiling window managers** (i3, Sway, Hyprland).
    
- Can integrate with **tmux** for advanced session management.