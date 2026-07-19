# VS Code Commands — Mac

**Example File:** `Chapter_01_JS_BASIC/01_HelloWorld.js`

```javascript
// Open terminal: Cmd + `
// Run: node Chapter_01_JS_BASIC/01_HelloWorld.js
console.log("Hello The Testing Academy!");
```

---

## ⌨️ Mac Keyboard Modifiers

| Symbol | Key |
|--------|-----|
| `⌘` | Command |
| `⌥` | Option (Alt) |
| `⇧` | Shift |
| `⌃` | Control |
| `␣` | Space |

---

## VS Code Shortcuts — Mac

### Navigation & Files
| Action | Shortcut |
|--------|----------|
| Command Palette | `⌘ + ⇧ + P` |
| Quick Open (File) | `⌘ + P` |
| Toggle Terminal | `⌃ + `` ` |
| Toggle Sidebar | `⌘ + B` |
| Close Tab | `⌘ + W` |
| Quick Switch Tab | `⌘ + Tab` |
| Split Editor | `⌘ + \` |
| Go to Line | `⌃ + G` |

### Editing
| Action | Shortcut |
|--------|----------|
| Save | `⌘ + S` |
| Save All | `⌘ + ⌥ + S` |
| Undo | `⌘ + Z` |
| Redo | `⌘ + ⇧ + Z` |
| Cut Line | `⌘ + X` (no selection) |
| Copy Line | `⌘ + C` (no selection) |
| Move Line Up/Down | `⌥ + ↑ / ↓` |
| Duplicate Line | `⇧ + ⌥ + ↑ / ↓` |
| Toggle Comment | `⌘ + /` |
| Block Comment | `⇧ + ⌥ + A` |
| Indent / Outdent | `⌘ + ]` / `⌘ + [` |
| Format Document | `⇧ + ⌥ + F` |
| Trigger Suggestion | `⌃ + ␣` |

### Selection & Search
| Action | Shortcut |
|--------|----------|
| Find | `⌘ + F` |
| Find & Replace | `⌘ + ⌥ + F` |
| Find in Files | `⌘ + ⇧ + F` |
| Add Selection (Multi-Cursor) | `⌘ + D` |
| Select All Occurrences | `⌘ + ⇧ + L` |
| Select Current Line | `⌘ + L` |
| Select Word | `⌘ + D` (repeated) |

### Code Intelligence
| Action | Shortcut |
|--------|----------|
| Go to Definition | `F12` |
| Peek Definition | `⌥ + F12` |
| Rename Symbol | `F2` |
| Go Back | `⌃ + -` |
| Go Forward | `⌃ + ⇧ + -` |

### View & Window
| Action | Shortcut |
|--------|----------|
| Toggle Word Wrap | `⌥ + Z` |
| Zoom In | `⌘ + =` |
| Zoom Out | `⌘ + -` |
| Open Settings | `⌘ + ,` |
| Open Extensions | `⌘ + ⇧ + X` |
| Source Control (Git) | `⌃ + ⇧ + G` |
| Explorer View | `⌘ + ⇧ + E` |
| Run and Debug | `⇧ + ⌘ + D` |

### Run / Debug
| Action | Shortcut |
|--------|----------|
| Start Debugging | `F5` |
| Run Without Debugging | `⌃ + F5` |
| Step Over | `F10` |
| Step Into | `F11` |
| Step Out | `⇧ + F11` |
| Stop | `⇧ + F5` |

---

## Terminal Commands — Mac (zsh/bash)

| # | Command | What it does |
|---|---------|-------------|
| 1 | `pwd` | Print working directory (where am I?) |
| 2 | `ls` | List files in current directory |
| 3 | `ls -la` | List all files (including hidden) with details |
| 4 | `cd <folder>` | Change directory |
| 5 | `cd ..` | Go up one directory |
| 6 | `cd ~` | Go to home directory |
| 7 | `mkdir <name>` | Create a new directory |
| 8 | `touch <file>` | Create a new empty file |
| 9 | `rm <file>` | Delete a file |
| 10 | `rm -rf <folder>` | Delete a folder (⚠️ careful) |
| 11 | `cp <src> <dest>` | Copy a file |
| 12 | `mv <src> <dest>` | Move / rename a file |
| 13 | `clear` | Clear terminal |
| 14 | `cat <file>` | Print file contents |
| 15 | `code .` | Open VS Code in current folder |
| 16 | `open .` | Open Finder in current folder |
| 17 | `node <file>` | Run a JS file with Node.js |
| 18 | `npm init` | Init a Node.js project |
| 19 | `npm install <pkg>` | Install a package |
| 20 | `npx <cmd>` | Run a package directly |
| 21 | `git status` | Check git status |
| 22 | `git add .` | Stage all changes |
| 23 | `git commit -m "msg"` | Commit with message |
| 24 | `git push` | Push to remote |
| 25 | `git log --oneline` | View compact commit history |
| 26 | `brew install <pkg>` | Install via Homebrew (Mac package manager) |

---

## Common VS Code Command Palette Commands

Open with `⌘ + ⇧ + P`, then type:

| Type this | What it does |
|-----------|-------------|
| `> Git: Commit` | Commit staged changes |
| `> Git: Push` | Push commits |
| `> Git: Pull` | Pull from remote |
| `> Git: Stage All` | Stage all changes |
| `> View: Toggle Terminal` | Open/close terminal |
| `> Preferences: Open Settings` | Open settings |
| `> Developer: Reload Window` | Restart VS Code |

---

## Pipeline: How a command gets executed

```
You press: ⌘ + ⇧ + P
       │
       ▼
  Command Palette opens
       │
       ▼
  You type: "Git: Commit"
       │
       ▼
  VS Code runs: git commit
       │
       ▼
  Result shown in Output / Terminal panel
```

---

## TL;DR

- Mac uses **⌘ (Command)** where Windows uses **Ctrl** — that's the main difference.
- Most VS Code shortcuts follow the pattern: `⌘ + key` for file ops, `⌥ + key` for line ops, `⇧ + modifier` for selection.
- Open the **integrated terminal** with `` ⌃ + ` `` and run `node`, `git`, and `npm` commands directly.
- Use `⌘ + ⇧ + P` for anything you can't remember — the Command Palette has it all.
