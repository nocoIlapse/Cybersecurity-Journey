## 📂 Navigation and Working with Files

### `cd`

Displays the current directory or changes the current working directory.

📌 Use `cd <directory>` to navigate to a folder and `cd ..` to move up one directory level.

---

### `dir`

Lists the files and directories in the current folder.

📌 Displays visible files and folders by default.

---

### `dir /a`

Lists all files and directories, including hidden items.

📌 Hidden files are not shown in a normal directory listing.

---

### `dir /s`

Searches for a file recursively through all subdirectories.

📌 The `/s` option searches every subfolder and displays the full path if the file is found.

---

### `type`

Displays the contents of a text file in the Command Prompt.

📌 Useful for reading text files without opening a text editor.

---

## 🖥️ System Information

### `whoami`

Displays the username of the currently logged-in user.

📌 Useful for verifying which account is currently in use.

---

### `hostname`

Displays the computer name.

📌 Useful for identifying a machine on a network.

---

### `systeminfo`

Displays detailed information about the operating system and hardware.

Common fields:

| Field | Description |
|--------|-------------|
| **OS Name** | Windows edition installed on the computer. |
| **OS Version** | Windows version and build number. |
| **System Type** | System architecture (32-bit or 64-bit). |
| **Host Name** | Computer name. |
| **BIOS Version** | BIOS information. |
| **Total Physical Memory** | Installed RAM. |

📌 Useful for gathering system information during troubleshooting or security assessments.

---

### `ipconfig`

Displays the current network configuration.

Common fields:

| Field | Description |
|--------|-------------|
| **IPv4 Address** | IP address assigned to the computer. |
| **Subnet Mask** | Defines the local network. |
| **Default Gateway** | Router used to access other networks. |

📌 Useful for checking network connectivity and IP configuration.
