## 🌀 **Hyprland**

**A modern, dynamic Wayland compositor** — like a window manager for Wayland (alternative to i3/Sway).  
It handles workspaces, windows, animations, and keybindings.

### ✨ Key Features:

- GPU-accelerated compositor
    
- Smooth animations and transitions
    
- Dynamic tiling + floating hybrid
    
- Highly configurable via `~/.config/hypr/hyprland.conf`
    

### ⚙️ Important Config Concepts:

- `exec-once = ...` → run programs at startup
    
- `bind = SUPER, Return, exec, alacritty` → keybind example
    
- `monitor = HDMI-A-1, preferred, auto, 1` → screen setup
    
- `workspace = name` → organize windows
    
- `decoration { blur = yes; rounding = 10 }` → UI styling
    

---

## 🎨 **Matugen**

**Dynamic color generator** for Wayland setups — inspired by Material You.  
It generates color schemes from wallpapers and applies them system-wide.

### 🧩 How It Works:

- Reads your wallpaper
    
- Extracts color palette (accent, background, etc.)
    
- Outputs a theme to match your wallpaper
    
- Integrates with Waybar, Rofi, GTK, etc.
    

### ⚙️ Usage:

`matugen --type wallpaper --file ~/Pictures/wall.jpg --theme dark`

👉 Updates colors in config files like:

- `~/.config/waybar/colors.css`
    
- `~/.config/rofi/colors.rasi`
    
- `~/.config/hypr/hyprland.conf`
    

---

## 🧭 **Waybar**

**Status bar** for Wayland compositors (like Polybar for X11).

### 🧱 Structure:

Config: `~/.config/waybar/config`  
Style: `~/.config/waybar/style.css`

### 🧩 Modules:

- `clock`, `cpu`, `memory`, `network`, `battery`, `tray`, etc.
    
- Custom scripts → show anything (e.g. weather, system info)
    

### ✨ Tips:

- Use `@import "colors.css";` in style.css for Matugen themes
    
- Can use `waybar -l info` to debug
    

---

## 🦄 **Rofi**

**Application launcher** — like an improved “Run” menu.

### 🪄 Uses:

- Launch apps
    
- Switch windows
    
- SSH launcher
    
- File browser (via plugins)
    

### ⚙️ Config:

File: `~/.config/rofi/config.rasi`  
Theme: `~/.config/rofi/theme.rasi`

Launch example:

`rofi -show drun`

Integrates with Matugen for dynamic colors:

`@import "~/.config/rofi/colors.rasi"`

---

## 🌈 **Swww**

**Wallpaper daemon** for Wayland — smooth transitions & animations.

### ✨ Features:

- Animated wallpaper changes
    
- Multiple monitors supported
    
- Compatible with Matugen (dynamic theme updates)
    

### ⚙️ Basic Usage:

`swww init swww img ~/Pictures/wallpaper.jpg --transition-type grow`

💡 Combine with Matugen:

`swww img ~/Pictures/wall.jpg && matugen --type wallpaper --file ~/Pictures/wall.jpg`

---

## 🖼️ **Hyprpaper**

**Lightweight wallpaper manager** for Hyprland (official).

### ⚙️ Config: `~/.config/hypr/hyprpaper.conf`

Example:

`preload = ~/Pictures/wall1.jpg preload = ~/Pictures/wall2.jpg wallpaper = HDMI-A-1, ~/Pictures/wall1.jpg`

### 🧩 Notes:

- Runs as `hyprpaper &` in `exec-once`
    
- Doesn’t animate (use `swww` if you want transitions)
    
- Great for static setups or when using scripts
    

---

## 🧠 **Recommended Setup Flow**

1. **Start Hyprland**
    
2. **Launch Hyprpaper or Swww**
    
3. **Run Matugen** → generate theme
    
4. **Reload Waybar + Rofi** → apply new colors
    
5. **Enjoy your dynamically themed Wayland desktop 💅**