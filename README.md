# DevOps_Journey
# Linux Command Line Cheat Sheet — Week 1
#phase 1

A collection of foundational Linux terminal commands learned during Week 1 of my DevOps roadmap.

## 1. Remote Connection & System Info
* `ssh` — Connects securely to a remote Linux server over a network.
  ```bash
  ssh user@host -p 2220
  * `man` — Displays the comprehensive reference manual for a command.
  ```bash
  man ls
  pwd — Displays the absolute path of the current working directory.
  pwd
  ls — Lists directory contents (-a includes hidden files, -l shows detailed permissions).
  ls -la
  cd — Changes the current directory.
  cd /var/log
  mkdir — Creates a new directory.
  mkdir devops-lab
  touch — Creates an empty file or updates the timestamp of an existing file.
  touch notes.txt
  cp — Copies files or directories from a source to a destination.
  cp notes.txt backup/
  mv — Moves or renames files and directories.
  mv script.sh backup/
  cat — Concatenates and prints the contents of a file to the terminal output.
  cat notes.txt
  file — Inspects magic bytes to determine the true format/type of a file.
  file ./-*
  find — Recursively searches a directory tree based on specific file attributes (type, size, permissions).
  find . -type f -size 1033c ! -executable

## Phase 2: Levels 6–12 (Core Utilities & Forensic Analysis)
## Overthewire  bandit war games
### 🛠️ Summary of Commands Mastered

| Level Range | Challenge Domain | Core Commands & Flags | Key Systems Engineering Concept |
| :--- | :--- | :--- | :--- |
| **Level 6 → 7** | System-wide Search | `find / -user ... -group ... -size ... 2>/dev/null` | Permissions, UID/GID filtering, byte sizes, suppressing `stderr`. |
| **Level 7 → 8** | Pattern Matching | `grep "pattern" filename` | Stream parsing and pattern filtering without heavy text editors. |
| **Level 8 → 9** | Unique Line Extraction | `sort filename \| uniq -u` | Pipeline chaining (`\|`) and adjacent duplicate detection requirements. |
| **Level 9 → 10** | Binary Data Analysis | `strings filename \| grep "="` | Scrapping human-readable ASCII out of compiled binary files. |
| **Level 10 → 11** | Base64 Decoding | `base64 -d filename` | Binary-to-text decoding and byte-to-ASCII stream conversion. |
| **Level 11 → 12** | Cipher Translation | `cat filename \| tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Substitution ciphers (ROT13) and character set mapping with `tr`. |
| **Level 12 → 13** | Hex Dumps & Decompression | `xxd -r`, `file`, `gzip -d`, `bzip2 -d`, `tar -xf` | Reversing hex dumps, inspecting magic numbers with `file`, nested archive extraction. |

