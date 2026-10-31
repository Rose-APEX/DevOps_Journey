# DevOps_Journey
# Linux Command Line Cheat Sheet — Week 1

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
