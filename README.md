# macOS Terminal Cheat Sheet
> Every command with a mental model — so it actually sticks.

**By [@Dav23Jonn76](https://x.com/Dav23Jonn76)**  
📖 [Full article on Notion](https://simple-yard-80d.notion.site/macOS-Terminal-Cheat-Sheet-3264c84f229880fcacc7dee99e3d5651)

---

If you've ever stared at a terminal window and felt completely lost — this is for you.

Most terminal guides dump 50 commands on you with zero context. This one is different. Every command has a **Mental Model** — a one-liner that explains *why* it works, not just *what* it does. That's the thing that actually makes it stick.

---

## Level 1 — Core Navigation

| Command | What It Does | Mental Model |
|---|---|---|
| `pwd` | Print current directory | GPS location |
| `ls` | List files/folders | Look around |
| `ls -la` | List all including hidden | X-ray vision |
| `cd folder` | Enter folder | Drive into street |
| `cd ..` | Go back one level | Reverse |
| `cd ~` | Go to home directory | Go home |
| `clear` | Clear screen | Clean windshield |

---

## Level 1 — File & Folder Control

| Command | What It Does | Mental Model |
|---|---|---|
| `mkdir folder` | Create folder | Build garage |
| `touch file.txt` | Create empty file | Blank paper |
| `cp file1 file2` | Copy file | Duplicate |
| `mv file1 file2` | Move / Rename | Relocate cargo |
| `rm file.txt` | Delete file | Trash |
| `rm -r folder` | Delete folder recursively | Bulldozer 🚨 |
| `open .` | Open folder in Finder | Open in GUI |

> ⚠️ **Warning:** `rm` has no undo. There's no trash. It's gone. Double-check before you hit Enter.

---

## Level 1 — Read & Write Files

| Command | What It Does | Mental Model |
|---|---|---|
| `cat file.txt` | Print file contents | Read aloud |
| `less file.txt` | Scroll through file | Paged reading |
| `head -n 10 file` | First 10 lines | Read the cover |
| `tail -n 10 file` | Last 10 lines | Read last page |
| `echo "hi" > file` | Write to file | Overwrite notepad |
| `echo "hi" >> file` | Append to file | Add to notepad |
| `nano file.txt` | Edit file in terminal | Open text editor |

---

## Level 1 — Python Basics

| Command | What It Does | Mental Model |
|---|---|---|
| `python3 script.py` | Run a script | Activate robot |
| `python3` | Open REPL | Talk to robot live |
| `pip install pkg` | Install package | Add a skill |
| `pip list` | List packages | Inventory skills |
| `pip freeze` | Export installed pkgs | Print manifest |
| `python3 -m venv env` | Create virtual env | Build sandbox |
| `source env/bin/activate` | Activate venv | Enter sandbox |

> 💡 **Pro tip:** Always use a virtual environment for projects. It keeps your packages isolated and prevents version conflicts.

---

## Level 2 — Advanced Terminal Control

| Command | What It Does | Mental Model |
|---|---|---|
| `grep 'text' file` | Search inside file | Ctrl+F for terminal |
| `find . -name file` | Find file recursively | Spotlight search |
| `\|` (pipe) | Pass output to next command | Conveyor belt |
| `> file.txt` | Redirect output to file | Save printout |
| `&&` | Run next command if success | Chain commands |
| `chmod 755 file` | Set permissions | Set access locks |
| `history` | Show past commands | Command log |

```bash
# Real example — find all .py files containing "error"
find . -name "*.py" | xargs grep "error"
```

---

## Level 2 — Processes & System

| Command | What It Does | Mental Model |
|---|---|---|
| `ps aux` | Show running processes | Task manager |
| `kill PID` | Stop process | Force quit |
| `kill -9 PID` | Force kill process | Hard power off |
| `top` | Live system monitor | Activity Monitor |
| `Ctrl + C` | Stop running command | Emergency stop |
| `Ctrl + Z` | Pause to background | Pause tape |
| `crontab -e` | Schedule task | Set an alarm |

---

## Level 2 — Network & Downloads

| Command | What It Does | Mental Model |
|---|---|---|
| `curl -O url` | Download file from URL | Fetch from web |
| `curl url` | Print URL response | Peek at a web page |
| `ping google.com` | Test connectivity | Throw a ping ball |
| `ifconfig` | Show network info | Check your IP |
| `ssh user@host` | Connect to remote server | Teleport in |
| `scp file user@host` | Copy file to server | Beam file over |
| `wget url` | Download from URL | Pull from web |

---

## Level 2 — Git Essentials

| Command | What It Does | Mental Model |
|---|---|---|
| `git init` | Start a repo | Open a logbook |
| `git status` | See what changed | Check the board |
| `git add .` | Stage all changes | Pack the box |
| `git commit -m ""` | Save a snapshot | Take a photo |
| `git push` | Upload to remote | Ship the box |
| `git pull` | Download latest | Receive shipment |
| `git clone url` | Copy a repo locally | Duplicate project |

```bash
# The daily Git workflow
git status
git add .
git commit -m "fix: updated config"
git push
```

---

## Level 3 — Power User Tricks

| Command | What It Does | Mental Model |
|---|---|---|
| `alias ll="ls -la"` | Create shortcut command | Custom hotkey |
| `export VAR=value` | Set env variable | Global setting |
| `echo $PATH` | See command search path | Road map |
| `which python3` | Find where command lives | Locate the tool |
| `xargs` | Pass output as arguments | Pipe into next job |
| `!!` | Repeat last command | Replay |
| `Ctrl + R` | Search command history | Rewind & search |

---

## Level 4 — Homebrew & Dev Setup

Install Homebrew first:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

| Command | What It Does | Mental Model |
|---|---|---|
| `brew install pkg` | Install macOS package | App store for devs |
| `brew list` | See installed packages | Inventory |
| `brew update` | Update Homebrew itself | Update the store |
| `brew upgrade pkg` | Upgrade a package | Update an app |
| `node -v` | Check Node version | Version check |
| `npm install` | Install JS packages | Load dependencies |
| `npm run dev` | Start dev server | Launch the app |

---

## Quick Reference: Keyboard Shortcuts

| Shortcut | What It Does |
|---|---|
| `Ctrl + C` | Kill current process |
| `Ctrl + Z` | Suspend to background |
| `Ctrl + R` | Search history |
| `Ctrl + L` | Clear screen |
| `Tab` | Autocomplete path/command |
| `↑ / ↓` | Navigate command history |
| `Ctrl + A` | Jump to start of line |
| `Ctrl + E` | Jump to end of line |

---

## The Mental Model That Changed Everything

Stop trying to memorize commands. Instead think:

- **Files are just boxes.** You can copy, move, look inside, or destroy them.
- **Commands are just verbs.** `grep` = search. `kill` = stop. `find` = locate.
- **Pipes `|` are conveyor belts.** Output of one command becomes input of the next.

Once you internalize those three things, you stop Googling and start *composing* commands from first principles.

---

*If this helped you, drop a ⭐ and share it with someone who just switched to Mac.*
