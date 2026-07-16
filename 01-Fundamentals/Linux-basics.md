# 🐧Linux CLI Cheatsheets

My personal notes on work with the Linux terminal, which I`m keeping while working through Stage 1 on TryHackMe.

## 📁Navigation and Working with Files

* `pwd` - print the current working directory.
* `ls` - list files and directories in the current folder.
* `ls -la` - show all files (including hidden ones) with detailed information.
* `cd [directory]` - change the current directory.
* `cd ..` - move one directory up.

---

## 📄Reading and Creating Files

* `cat [file]` - display the contents of a file.
* `touch [file]` - create a new empty file.
* `nano [file]` - open or edit a file using the Nano text editor.
* `cp [source] [destination]` - copy files or directories.
* `mv [source] [destination]` - move or rename files and directories.
* `rm [file]` - remove a file.
* `mkdir [directory]` - create a new directory.
* `rmdir [directory]` - remove a directory.

---

## 🖥️User & System Information

* `whoami` - display the current logged-in user.
* `uname` - display the operating system name.
* `uname -a` - display detailed system information (kernel, hostname, architecture, etc.).
* `hostname` - display the system hostname.

---

## 💾Disk Usage

* `df -h` - display disk usage in a human-readable format.
* `du -sh [directory]` - display the total size of a directory.

---

## 📂System Information Files

* `/etc/os-release` - contains information about the Linux distribution.
* `cat /etc/os-release` - display Linux distribution information.
