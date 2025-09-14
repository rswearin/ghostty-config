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
keybind = ctrl+space>s>a=new_split:left
keybind = ctrl+space>s>d=new_split:right
keybind = ctrl+space>s>w=new_split:up
keybind = ctrl+space>s>s=new_split:down
keybind = ctrl+space>s>z=new_split:auto

# Navigate
keybind = ctrl+space>n>a=goto_split:left
keybind = ctrl+space>n>d=goto_split:right
keybind = ctrl+space>n>w=goto_split:up
keybind = ctrl+space>n>s=goto_split:down

# Resize
keybind = ctrl+space>r>a=resize_split:left,30
keybind = ctrl+space>r>d=resize_split:right,30
keybind = ctrl+space>r>w=resize_split:up,30
keybind = ctrl+space>r>s=resize_split:down,30

# Layout management
keybind = ctrl+space>e=equalize_splits
keybind = ctrl+space>z=toggle_split_zoom
keybind = ctrl+space>x=close_surface

# Tabs (optional)
keybind = ctrl+space>t=new_tab
keybind = ctrl+space>[=previous_tab
keybind = ctrl+space>]=next_tab

# QoL
keybind = ctrl+space>c=reload_config
keybind = ctrl+space>o=open_config

# Quick Terminal (macOS)
# Global drop-down on ⌘+`
keybind = global:cmd+grave_accent=toggle_quick_terminal
quick-terminal-position = bottom
quick-terminal-screen = main
quick-terminal-autohide = true
quick-terminal-animation-duration = 0.20
macos-non-native-fullscreen = true

```
3. Optional shell customizations

nano ~/.zshrc

Paste in the following:
```
# Colorful zsh prompt
autoload -U colors && colors
autoload -Uz vcs_info
precmd() { vcs_info }
setopt prompt_subst
if [[ "$TERM_PROGRAM" == "ghostty" ]]; then
  export TERM=xterm-256color
fi

# Format: username@host path [branch]
PROMPT='%F{green}%n@%m %F{blue}%~ %F{yellow}${vcs_info_msg_0_}%f ➜ '
zstyle ':vcs_info:git:*' formats '[%b]'
```
source ~/.zshrc


---

## ⌨️ Keybindings Overview

### Splits

* `Ctrl + Space, s, a` → new split left
* `Ctrl + Space, s, d` → new split right
* `Ctrl + Space, s, w` → new split up
* `Ctrl + Space, s, s` → new split down
* `Ctrl + Space, s, z` → auto split

### Navigation

* `Ctrl + Space, n, a` → move focus left
* `Ctrl + Space, n, d` → move focus right
* `Ctrl + Space, n, w` → move focus up
* `Ctrl + Space, n, s` → move focus down

### Resize

* `Ctrl + Space, r, a` → resize in that direction
* `Ctrl + Space, r, d` → resize in that direction
* `Ctrl + Space, r, w` → resize in that direction
* `Ctrl + Space, r, s` → resize in that direction

### Layout

* `Ctrl + Space, e` → equalize splits
* `Ctrl + Space, z` → zoom/unzoom current split
* `Ctrl + Space, x` → close current split

### Tabs (optional)

* `Ctrl + Space, t` → new tab
* `Ctrl + Space, [` → previous tab
* `Ctrl + Space, ]` → next tab

### QoL

* `Ctrl + Space, c` → reload config
* `Ctrl + Space, o` → open config

### Quick Terminal (macOS)

* `⌘ + backtick` → for global quick terminal (requires Accessibility permission on macOS - grant macOS Accessibility when prompted or enable in Settings → Privacy & Security → Accessibility)
