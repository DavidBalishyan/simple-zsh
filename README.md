# 🌿 simple.zsh-theme

A minimal yet informative **Zsh theme** focused on clarity, speed, and subtle color hints.  
It displays user, host, current directory, Git branch (with dirty state), exit status, and the duration of the last command - all in a clean layout.

---

## ✨ Features

- 🧑‍💻 **User and Host** - hows `user@machine`
- 📂 **Current Directory** - Highlights the present working directory
- 🌿 **Git Status** - Displays the current Git branch and a `*` if the repo is dirty
- ❌ **Exit Code** - Shows a red ✘ and exit code if the last command failed
- 🎨 **Colorful and Minimal** - Uses Zsh’s built-in color system (`autoload -U colors && colors`)

---

## 🧩 Installation

### 1. Clone or download the theme

```bash
mkdir -p ~/.zsh/themes
curl -o ~/.zsh/themes/simple.zsh-theme https://raw.githubusercontent.com/DavidBalishyan/simple-zsh/main/simple.zsh-theme
```

### 2. Load it in your `.zshrc`

Add this line to your `~/.zshrc`:

```bash
source ~/.zsh/themes/simple.zsh-theme
```

or, if you’re using **Oh My Zsh**, copy it to your theme folder and set it as the theme:

```bash
cp simple.zsh-theme ~/.oh-my-zsh/custom/themes/
```

Then edit `.zshrc`:

```bash
ZSH_THEME="simple"
```

---

## 🖼️ Prompt Layout

**Left Prompt (`PROMPT`):**

```
username@hostname ~/current/directory git:(branch*) $
```

**Right Prompt (`RPROMPT`):**

```
✘ 1
```

> ✘ only shows if the last command failed.

---

## ⚙️ Code Overview

- **`git_prompt_info`** - Detects branch name and dirty state
- **`build_prompt`** - Builds the left-side prompt (username, dir, git)
- **`build_rprompt`** - Builds the right-side prompt (exit code, time)

---

## 🧠 Example

```
david@debian ~/projects/simple git:(main*) $
```

Right side -> `✘ 1`

---

## 🪄 Customization Tips

- To change colors, edit the `%{$fg[color]%}` parts.

---

## 📄 License

MIT License © 2025 DavidBalishyan

---

**simple.zsh-theme - Less noise, more info.**
