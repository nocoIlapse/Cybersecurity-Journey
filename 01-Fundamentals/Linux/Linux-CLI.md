# 🐧 Linux Command Line Basics

## 📖 Overview

The Linux Command Line Interface (CLI) is a text-based interface used to interact with the operating system.

Unlike a Graphical User Interface (GUI), the CLI allows users to execute commands directly, automate tasks using scripts, and efficiently manage files, processes, and system resources.

Learning the Linux CLI is a fundamental skill for system administrators, developers, and cybersecurity professionals.

---

## 🎯 Why Is It Important?

Most Linux servers run without a graphical interface, making the command line the primary way to manage systems.

For cybersecurity professionals, the CLI is essential for:

- Navigating the file system
- Managing files and directories
- Inspecting system information
- Automating repetitive tasks
- Performing enumeration during penetration tests
- Executing security tools

---

# 📁 Navigation and Working with Files

## `pwd`

### Purpose

Displays the absolute path of the current working directory.

### Syntax

```bash
pwd
```


Output:

```text
/home/kali/Documents
```

### Notes

Useful when you are unsure of your current location in the filesystem.

---

## `ls`

### Purpose

Lists files and directories.

### Syntax

```bash
ls
```

### Common Options

| Option | Description |
|---------|-------------|
| `-l` | Long listing format |
| `-a` | Show hidden files |
| `-h` | Human-readable file sizes |
| `-la` | Long listing including hidden files |

---

## `cd`

### Purpose

Changes the current working directory.

### Syntax

```bash
cd [directory]
```

```bash
cd ..
```

```bash
cd ~
```

### Notes

- `..` → Parent directory
- `~` → Home directory

---

# 📄 Reading and Creating Files

## `cat`

### Purpose

Displays the contents of a file.

### Syntax

```bash
cat filename.txt
```

---

## `touch`

### Purpose

Creates a new empty file or updates the file timestamp.

### Example

```bash
touch report.txt
```

---

## `nano`

### Purpose

Opens a file in the Nano text editor.


Useful shortcuts:

| Shortcut | Action |
|-----------|--------|
| `Ctrl + O` | Save |
| `Ctrl + X` | Exit |
| `Ctrl + K` | Cut line |
| `Ctrl + U` | Paste line |

---

## `cp`

### Purpose

Copies files or directories.


Copy directories:

```bash
cp -r folder backup/
```

---

## `mv`

### Purpose

Moves or renames files and directories.


Rename:

```bash
mv old.txt new.txt
```

Move:

```bash
mv report.txt Documents/
```

---

## `rm`

### Purpose

Removes files.


```bash
rm file.txt
```

Delete directory recursively:

```bash
rm -r folder
```

⚠️ Files deleted with `rm` cannot normally be recovered.

---

## `mkdir`

### Purpose

Creates a directory.


```bash
mkdir Projects
```

Create nested directories:

```bash
mkdir -p Notes/Linux
```

---

## `rmdir`

### Purpose

Removes an empty directory.


```bash
rmdir OldFolder
```

---

# 🖥️ User & System Information

## `whoami`

Displays the currently logged-in user.

```bash
whoami
```

---

## `hostname`

Displays the computer hostname.

```bash
hostname
```

---

## `uname`

Displays kernel information.

```bash
uname
```

Detailed information:

```bash
uname -a
```

---

# 💾 Disk Usage

## `df`

Displays filesystem disk usage.

```bash
df -h
```

---

## `du`

Displays directory size.

```bash
du -sh Downloads
```

---

# 📂 System Information Files

## `/etc/os-release`

Contains information about the Linux distribution.

Display it with:

```bash
cat /etc/os-release
```

Example output:

```text
NAME="Ubuntu"
VERSION="24.04 LTS"
ID=ubuntu
```

---

## 🔒 Security Notes

- Be careful when using `rm -r`, especially as the root user.
- Avoid running unknown commands with `sudo`.
- Verify your current directory using `pwd` before deleting files.
- Check command syntax before executing destructive operations.

---

## 📝 Key Takeaways

- The CLI is the primary way to manage Linux systems.
- Commands can be combined to perform powerful administrative tasks.
- Understanding file navigation is essential before learning scripting or penetration testing.
- Always verify destructive commands before executing them.
