# 💫 Tmux Configuration

A clean and modern **tmux** setup designed for speed, clarity, and comfort.  
Includes popup-based session switching, true color support, and vim-style navigation — all with a minimalist theme.

---

## ⚙️ Features

✨ True Color Support (`terminal-overrides: RGB`)  
🖱️ Mouse Mode Enabled  
⚡ Zero Escape Delay (`escape-time 0`)  
🔢 Windows & Panes Start From 1  
🧭 Vim-Style Navigation (`hjkl` keys)  
🪄 Popup Session Switcher via [`tmux-sessionx`](https://github.com/omerxx/tmux-sessionx)  
🌈 Clean, Minimal Status Line Theme  
🧩 Plugin Manager via [`tpm`](https://github.com/tmux-plugins/tpm)

---

## 📦 Plugins

| 🧩 Plugin | 🔍 Description |
|-----------|----------------|
| [`tmux-plugins/tpm`](https://github.com/tmux-plugins/tpm) | Plugin manager for tmux |
| [`tmux-plugins/tmux-sensible`](https://github.com/tmux-plugins/tmux-sensible) | Smart, sane defaults for tmux |
| [`omerxx/tmux-sessionx`](https://github.com/omerxx/tmux-sessionx) | Fuzzy session switcher with preview popup |

---

## 🎹 Keybindings

### 🔑 Prefix
> **Prefix key:** `Ctrl + Space`

---

### 🧭 Pane Navigation
| Keys | Action |
|------|---------|
| `h` / `j` / `k` / `l` | Move left / down / up / right |
| `H` / `J` / `K` / `L` | Resize left / down / up / right |
| `Alt + h/j/k/l` | Move between panes (no prefix) |
| `f` or `Alt + f` | Toggle zoom (maximize/minimize pane) |

---

### 🪟 Window Management
| Keys | Action |
|------|---------|
| `Ctrl + n` | Next window |
| `Ctrl + p` | Previous window |
| `Alt + [1–9]` | Jump directly to window number |

---

### 🔲 Splitting Panes
| Keys | Action |
|------|---------|
| `|` | Split horizontally |
| `-` | Split vertically |

---

### 💡 Miscellaneous
| Keys | Action |
|------|---------|
| `e` | Choose window (popup mode) |
| `q` | Detach tmux client |
| `Alt + o` | Open **SessionX** popup to switch/create sessions |

---

## 🎨 Theme Overview

| Element | Style |
|----------|--------|
| **Pane Border (Inactive)** | Black / Bright |
| **Pane Border (Active)** | Magenta |
| **Status Line** | Transparent background, bright black text |
| **Status Right** | Shows current session name `#S` |
| **Window (Current)** | Magenta (yellow when zoomed) |
| **Bell Notification** | Red |

---

## 🚀 Installation

### 1️⃣ Clone TPM
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

### 2️⃣ Copy Configuration
```bash
cp tmux.conf ~/.tmux.conf
```

### 3️⃣ Reload tmux
```bash
tmux source ~/.tmux.conf
```

### 4️⃣ Install Plugins
Inside tmux, press:
```
prefix + I
```

> 🧠 **Tip:** The prefix key is `Ctrl + Space`.

---

## 🔧 Quick Commands

Reload configuration on the fly:
```bash
tmux source-file ~/.tmux.conf
```

List all sessions:
```bash
tmux ls
```

Kill a specific session:
```bash
tmux kill-session -t <session-name>
```

Detach from tmux:
```bash
prefix + q
```

---

## 💬 Notes

- You can customize keybindings, border colors, or SessionX options in your `~/.tmux.conf`.
- The popup session management (`Alt + o`) requires **tmux ≥ 3.2** for popup support.

---

## 🧑‍💻 Author

**Ezra Lawrence**  
🗂️ Project: Personal Tmux Config  
💾 License: MIT  

---

### 🧠 Bonus Tip

Want to automatically start tmux when you open a terminal?

Add this to your `.bashrc` or `.zshrc`:

```bash
# Auto-start tmux if not already inside one
[ -z "$TMUX" ] && tmux
```

---

⭐ **Enjoy your new tmux workflow!**
