# ghostty-config
macOS Ghostty tiling setup

---

## Setup

1. Open the Ghostty config file with **`⌘ + ,`** (Command + Comma) inside Ghostty.

2. Paste the configuration **after the comment block message**. 

```
# Looks
font-family = Iosevka
window-padding-x = 4
window-padding-y = 4
background-opacity = 1.0
cursor-style = bar
theme = OneHalfDark

# Leader-based tiling (Ctrl+Space as leader)
# Splits
keybind = ctrl+space>l=new_split:left
keybind = ctrl+space>r=new_split:right
keybind = ctrl+space>u=new_split:up
keybind = ctrl+space>d=new_split:down
keybind = ctrl+space>a=new_split:auto

# Navigate (uppercase)
keybind = ctrl+space>L=goto_split:left
keybind = ctrl+space>R=goto_split:right
keybind = ctrl+space>U=goto_split:up
keybind = ctrl+space>D=goto_split:down

# Resize (Shift+direction)
keybind = ctrl+space>shift+l=resize_split:left,30
keybind = ctrl+space>shift+r=resize_split:right,30
keybind = ctrl+space>shift+u=resize_split:up,30
keybind = ctrl+space>shift+d=resize_split:down,30

# Layout management
keybind = ctrl+space>e=equalize_splits
keybind = ctrl+space>z=toggle_split_zoom
keybind = ctrl+space>x=close_surface

# Tabs (optional)
keybind = ctrl+space>t=new_tab
keybind = ctrl+space>[=previous_tab
keybind = ctrl+space>]=next_tab

# QoL
keybind = ctrl+space>r=reload_config
keybind = ctrl+space>o=open_config
```

---

## ⌨️ Keybindings Overview

### Splits

* `Ctrl + Space, l` → new split left
* `Ctrl + Space, r` → new split right
* `Ctrl + Space, u` → new split up
* `Ctrl + Space, d` → new split down
* `Ctrl + Space, a` → auto split

### Navigation

* `Ctrl + Space, L` → move focus left
* `Ctrl + Space, R` → move focus right
* `Ctrl + Space, U` → move focus up
* `Ctrl + Space, D` → move focus down

### Resize

* `Ctrl + Space, Shift+l/r/u/d` → resize in that direction

### Layout

* `Ctrl + Space, e` → equalize splits
* `Ctrl + Space, z` → zoom/unzoom current split
* `Ctrl + Space, x` → close current split

### Tabs (optional)

* `Ctrl + Space, t` → new tab
* `Ctrl + Space, [` → previous tab
* `Ctrl + Space, ]` → next tab

### QoL

* `Ctrl + Space, r` → reload config
* `Ctrl + Space, o` → open config