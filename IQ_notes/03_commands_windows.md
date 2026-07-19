# VS Code Commands — Windows

**Example File:** `Chapter_01_JS_BASIC/01_HelloWorld.js`

```javascript
// Open terminal: Ctrl + `
// Run: node Chapter_01_JS_BASIC/01_HelloWorld.js
console.log("Hello The Testing Academy!");
```

---

## VS Code Shortcuts — Windows

### Navigation & Files
| Action | Shortcut |
|--------|----------|
| Command Palette | `Ctrl + Shift + P` |
| Quick Open (File) | `Ctrl + P` |
| Toggle Terminal | `Ctrl + `` ` |
| Toggle Sidebar | `Ctrl + B` |
| Close Tab | `Ctrl + W` |
| Quick Switch Tab | `Ctrl + Tab` |
| Split Editor | `Ctrl + \` |
| Go to Line | `Ctrl + G` |

### Editing
| Action | Shortcut |
|--------|----------|
| Save | `Ctrl + S` |
| Save All | `Ctrl + K, S` |
| Undo | `Ctrl + Z` |
| Redo | `Ctrl + Y` |
| Cut Line | `Ctrl + X` (no selection) |
| Copy Line | `Ctrl + C` (no selection) |
| Move Line Up/Down | `Alt + ↑ / ↓` |
| Duplicate Line | `Shift + Alt + ↑ / ↓` |
| Toggle Comment | `Ctrl + /` |
| Block Comment | `Shift + Alt + A` |
| Indent / Outdent | `Tab` / `Shift + Tab` |
| Format Document | `Shift + Alt + F` |
| Trigger Suggestion | `Ctrl + Space` |

### Selection & Search
| Action | Shortcut |
|--------|----------|
| Find | `Ctrl + F` |
| Find & Replace | `Ctrl + H` |
| Find in Files | `Ctrl + Shift + F` |
| Add Selection (Multi-Cursor) | `Ctrl + D` |
| Select All Occurrences | `Ctrl + Shift + L` |
| Select Current Line | `Ctrl + L` |
| Select Word | `Ctrl + D` (repeated) |

### Code Intelligence
| Action | Shortcut |
|--------|----------|
| Go to Definition | `F12` |
| Peek Definition | `Alt + F12` |
| Rename Symbol | `F2` |
| Go Back | `Ctrl + Alt + -` |
| Go Forward | `Ctrl + Shift + -` |

### View & Window
| Action | Shortcut |
|--------|----------|
| Toggle Word Wrap | `Alt + Z` |
| Zoom In | `Ctrl + =` |
| Zoom Out | `Ctrl + -` |
| Open Settings | `Ctrl + ,` |
| Open Extensions | `Ctrl + Shift + X` |
| Source Control (Git) | `Ctrl + Shift + G` |
| Explorer View | `Ctrl + Shift + E` |
| Run and Debug | `Ctrl + Shift + D` |

### Run / Debug
| Action | Shortcut |
|--------|----------|
| Start Debugging | `F5` |
| Run Without Debugging | `Ctrl + F5` |
| Step Over | `F10` |
| Step Into | `F11` |
| Step Out | `Shift + F11` |
| Stop | `Shift + F5` |

---

## Terminal Commands — Windows (PowerShell / Cmd)

### PowerShell
| # | Command | What it does |
|---|---------|-------------|
| 1 | `pwd` | Print working directory (where am I?) |
| 2 | `Get-ChildItem` or `ls` or `dir` | List files in directory |
| 3 | `cd <folder>` | Change directory |
| 4 | `cd ..` | Go up one directory |
| 5 | `cd ~` | Go to user home directory |
| 6 | `mkdir <name>` | Create a new directory |
| 7 | `New-Item <file>` or `ni <file>` | Create a new file |
| 8 | `Remove-Item <file>` or `del <file>` | Delete a file |
| 9 | `Copy-Item <src> <dest>` or `cp` | Copy a file |
| 10 | `Move-Item <src> <dest>` or `mv` | Move / rename |
| 11 | `Clear-Host` or `cls` | Clear terminal |
| 12 | `Get-Content <file>` or `cat <file>` | Print file contents |
| 13 | `code .` | Open VS Code in current folder |
| 14 | `start .` | Open File Explorer in current folder |
| 15 | `node <file>` | Run a JS file with Node.js |
| 16 | `npm init` | Init a Node.js project |
| 17 | `npm install <pkg>` | Install a package |
| 18 | `npx <cmd>` | Run a package directly |

### Command Prompt (cmd.exe)
| # | Command | What it does |
|---|---------|-------------|
| 1 | `cd` | Print working directory |
| 2 | `dir` | List files in directory |
| 3 | `cd <folder>` | Change directory |
| 4 | `cd ..` | Go up one directory |
| 5 | `cd %USERPROFILE%` | Go to user home |
| 6 | `mkdir <name>` | Create a new directory |
| 7 | `type nul > <file>` | Create a new empty file |
| 8 | `del <file>` | Delete a file |
| 9 | `copy <src> <dest>` | Copy a file |
| 10 | `move <src> <dest>` | Move / rename |
| 11 | `cls` | Clear terminal |
| 12 | `type <file>` | Print file contents |
| 13 | `code .` | Open VS Code |
| 14 | `explorer .` | Open File Explorer |

### Git Commands (same on both shells)
| # | Command | What it does |
|---|---------|-------------|
| 1 | `git status` | Check git status |
| 2 | `git add .` | Stage all changes |
| 3 | `git commit -m "msg"` | Commit with message |
| 4 | `git push` | Push to remote |
| 5 | `git pull` | Pull from remote |
| 6 | `git log --oneline` | View compact commit history |

---

## Common VS Code Command Palette Commands

Open with `Ctrl + Shift + P`, then type:

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
You press: Ctrl + Shift + P
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

- **Windows** uses **Ctrl** and **Alt** modifiers (Mac uses Cmd and Option) — that's the main difference.
- In PowerShell you can use both Unix-style commands (`ls`, `cat`, `pwd`) and Windows-style (`dir`, `type`, `cls`).
- In Command Prompt (`cmd.exe`), use traditional DOS commands (`dir`, `type`, `cls`).
- `Ctrl + Shift + P` opens the Command Palette — learn this one shortcut and you can do anything.
- Toggle the integrated terminal with `` Ctrl + ` `` — most git/node/npm commands run there.
