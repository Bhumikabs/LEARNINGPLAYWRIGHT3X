# VS Code Commands — General Reference

**Example File:** Any `.js` file in the project

```javascript
// Open terminal: Ctrl+` (Windows) / Cmd+` (Mac)
// Run: node Chapter_01_JS_BASIC/01_HelloWorld.js
console.log("Hello The Testing Academy!");
```

---

## VS Code Keyboard Shortcuts

| # | Action | Windows / Linux | Mac |
|---|--------|----------------|-----|
| 1 | **Command Palette** | `Ctrl + Shift + P` | `Cmd + Shift + P` |
| 2 | **Quick Open (File)** | `Ctrl + P` | `Cmd + P` |
| 3 | **Toggle Terminal** | `Ctrl + `` ` | `Ctrl + `` ` |
| 4 | **Toggle Sidebar** | `Ctrl + B` | `Cmd + B` |
| 5 | **Save File** | `Ctrl + S` | `Cmd + S` |
| 6 | **Save All** | `Ctrl + K, S` | `Cmd + K, S` |
| 7 | **Close Tab** | `Ctrl + W` | `Cmd + W` |
| 8 | **Undo** | `Ctrl + Z` | `Cmd + Z` |
| 9 | **Redo** | `Ctrl + Y` | `Cmd + Shift + Z` |
| 10 | **Cut Line** | `Ctrl + X` (no selection) | `Cmd + X` (no selection) |
| 11 | **Copy Line** | `Ctrl + C` (no selection) | `Cmd + C` (no selection) |
| 12 | **Move Line Up/Down** | `Alt + ↑ / ↓` | `Option + ↑ / ↓` |
| 13 | **Duplicate Line** | `Shift + Alt + ↑ / ↓` | `Shift + Option + ↑ / ↓` |
| 14 | **Toggle Comment** | `Ctrl + /` | `Cmd + /` |
| 15 | **Block Comment** | `Shift + Alt + A` | `Shift + Option + A` |
| 16 | **Indent / Outdent** | `Tab` / `Shift + Tab` | `Tab` / `Shift + Tab` |
| 17 | **Find** | `Ctrl + F` | `Cmd + F` |
| 18 | **Find & Replace** | `Ctrl + H` | `Cmd + H` |
| 19 | **Go to Definition** | `F12` | `F12` |
| 20 | **Peek Definition** | `Alt + F12` | `Option + F12` |
| 21 | **Rename Symbol** | `F2` | `F2` |
| 22 | **Format Document** | `Shift + Alt + F` | `Shift + Option + F` |
| 23 | **Multi-Cursor (Add)** | `Ctrl + D` | `Cmd + D` |
| 24 | **Select All Occurrences** | `Ctrl + Shift + L` | `Cmd + Shift + L` |
| 25 | **Toggle Word Wrap** | `Alt + Z` | `Option + Z` |
| 26 | **Zoom In / Out** | `Ctrl + =` / `Ctrl + -` | `Cmd + =` / `Cmd + -` |
| 27 | **Open Settings** | `Ctrl + ,` | `Cmd + ,` |
| 28 | **Open Extensions** | `Ctrl + Shift + X` | `Cmd + Shift + X` |
| 29 | **Source Control (Git)** | `Ctrl + Shift + G` | `Cmd + Shift + G` |
| 30 | **Run / Debug** | `F5` | `F5` |

---

## VS Code Command Palette Commands

Open with `Ctrl/Cmd + Shift + P`, then type:

| Command | What it does |
|---------|-------------|
| `> Git: Commit` | Commit staged changes |
| `> Git: Push` | Push commits to remote |
| `> Git: Pull` | Pull latest from remote |
| `> Git: Stage All` | Stage all changes |
| `> View: Toggle Terminal` | Open/close terminal panel |
| `> File: Save` | Save current file |
| `> Developer: Reload Window` | Restart VS Code window |
| `> Preferences: Open Settings` | Open settings UI |
| `> Extensions: Install Extensions` | Browse & install extensions |
| `> Transform: To Lowercase / Uppercase` | Change text case |

---

## Common Terminal Commands

| # | Command | What it does |
|---|---------|-------------|
| 1 | `node <file.js>` | Run a JavaScript file with Node.js |
| 2 | `npm init` | Initialize a new Node.js project (`package.json`) |
| 3 | `npm install <pkg>` | Install a package |
| 4 | `npx <cmd>` | Run a package without installing globally |
| 5 | `git status` | Show current repo state |
| 6 | `git add <file>` | Stage a file for commit |
| 7 | `git add .` | Stage all changes |
| 8 | `git commit -m "msg"` | Commit staged changes |
| 9 | `git push` | Push commits to remote |
| 10 | `git pull` | Pull latest from remote |
| 11 | `git log --oneline` | Show commit history (compact) |
| 12 | `cd <folder>` | Change directory |
| 13 | `mkdir <name>` | Create a new directory |
| 14 | `code .` | Open VS Code in current directory |
| 15 | `clear` (Win: `cls`) | Clear terminal output |

---

## How commands flow in VS Code

```
┌────────────────────────────────────────────────────────────┐
│                     VS CODE EDITOR                          │
│                                                             │
│  ┌──────────────────────────────────────────────────────┐   │
│  │  Keyboard Shortcut  (e.g. Ctrl + Shift + P)          │   │
│  │       │                                               │   │
│  │       ▼                                               │   │
│  │  Command Palette → Type "Git: Commit"                 │   │
│  │       │                                               │   │
│  │       ▼                                               │   │
│  │  Command Executes (Git commit happens)                │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌──────────────────────────────────────────────────────┐   │
│  │  Integrated Terminal  (Ctrl + `)                      │   │
│  │       │                                               │   │
│  │       ▼                                               │   │
│  │  Type: node file.js  →  Node runs the file            │   │
│  │  Type: git push      →  Git pushes to remote          │   │
│  │  Type: npm install   →  NPM installs packages          │   │
│  └──────────────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────┘
```

---

## TL;DR

- **VS Code shortcuts** are the fastest way to navigate and edit — memorize the ones you use most (Command Palette, Terminal toggle, Save, Find).
- **Command Palette** (`Ctrl/Cmd + Shift + P`) gives you access to every VS Code feature by typing — no menu hunting.
- **Terminal commands** (`git`, `node`, `npm`) are typed directly in the integrated terminal (`Ctrl/Cmd + `` `).
- The same VS Code shortcuts work on both Mac and Windows — just swap `Ctrl` with `Cmd` and `Alt` with `Option`.
