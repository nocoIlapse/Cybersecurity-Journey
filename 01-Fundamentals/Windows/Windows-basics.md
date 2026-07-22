# 🪟 Windows Command Prompt Basics

## 📖 Overview

The **Command Prompt (CMD)** is a command-line interpreter included with Microsoft Windows.

It allows users to interact with the operating system by executing text-based commands instead of using the Graphical User Interface (GUI).

Although PowerShell has become the preferred shell for modern Windows administration, CMD is still widely used for system administration, troubleshooting, scripting, and penetration testing.

---

## 🎯 Why Is It Important?

Understanding basic CMD commands is essential because they allow you to:

- Navigate the Windows file system.
- Manage files and directories.
- Gather system information.
- Troubleshoot network problems.
- Perform system enumeration during penetration tests.

---

# 📂 Navigation and Working with Files

## `cd`

### Purpose

Changes the current working directory.

### Syntax

```cmd
cd <directory>
```

```cmd
cd ..
```

```cmd
cd \
```

### Notes

- `cd ..` moves one directory up.
- `cd \` returns to the root of the current drive.
- Running `cd` without arguments displays the current directory.

---

## `dir`

### Purpose

Lists files and directories in the current location.

### Syntax

```cmd
dir
```

### Common Options

| Option | Description |
|---------|-------------|
| `/a` | Show hidden and system files |
| `/s` | Search recursively through subdirectories |
| `/b` | Display only file names |
| `/o` | Sort output |


### Notes

`dir` is one of the most frequently used commands for exploring the Windows filesystem.

---

## `type`

### Purpose

Displays the contents of a text file directly in the Command Prompt.

### Syntax

```cmd
type filename.txt
```


### Notes

Useful for quickly reading configuration files, logs, or scripts without opening a text editor.

---

# 🖥️ System Information

## `whoami`

### Purpose

Displays the username of the currently logged-in user.

### Example

```cmd
whoami
```

### Notes

Useful for confirming the current user account and identifying the security context of a process.

---

## `hostname`

### Purpose

Displays the computer name.


### Notes

Useful for identifying a device within a network.

---

## `systeminfo`

### Purpose

Displays detailed information about the operating system, hardware, and installed updates.


### Common Fields

| Field | Description |
|--------|-------------|
| **OS Name** | Installed Windows edition |
| **OS Version** | Windows version and build |
| **System Type** | System architecture (32-bit or 64-bit) |
| **Host Name** | Computer name |
| **BIOS Version** | BIOS information |
| **Total Physical Memory** | Installed RAM |

### Notes

Frequently used during system enumeration and troubleshooting.

---

## `ipconfig`

### Purpose

Displays the current TCP/IP network configuration.


Display detailed information:

```cmd
ipconfig /all
```

### Common Fields

| Field | Description |
|--------|-------------|
| **IPv4 Address** | Current IP address |
| **Subnet Mask** | Defines the local network |
| **Default Gateway** | Router used to reach other networks |

### Notes

Useful for diagnosing network connectivity issues and verifying IP configuration.

---

## 🔒 Security Notes

- Commands such as `systeminfo`, `hostname`, and `ipconfig` are commonly used during the **enumeration phase** of a penetration test.
- The information they reveal can help identify operating system versions, network configuration, and potential attack vectors.
- Avoid exposing detailed system information to unauthorized users.

---

## ⚠️ Common Mistakes

- Assuming `dir` displays hidden files by default.
- Forgetting that `cd` without arguments displays the current directory.
- Using `ipconfig` when more detailed information requires `ipconfig /all`.
- Confusing the computer name (`hostname`) with the logged-in username (`whoami`).

---

## 📝 Key Takeaways

- CMD is the traditional command-line interpreter for Windows.
- Basic commands allow navigation, file management, and system administration.
- `systeminfo` and `ipconfig` are valuable during troubleshooting and security assessments.
- Understanding CMD commands provides a strong foundation before learning PowerShell.
