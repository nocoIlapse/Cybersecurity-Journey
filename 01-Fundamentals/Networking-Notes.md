# 🌐 Networking Cheatsheet

My personal notes on networking fundamentals, which I'm keeping while studying Stage 1 on TryHackMe.

## 📡 Basic Networking Commands
* `ip a` — show network interfaces and IP addresses.
* `ip route` — display the routing table.
* `ping [host]` — check connectivity to a host.
* `traceroute [host]` — show the path packets take to a destination.
* `nslookup [domain]` — find the IP address of a domain.
* `dig [domain]` — get detailed DNS information.
* `netstat -tuln` — display listening ports and active connections.
* `ss -tuln` — modern alternative to `netstat`.
* `curl [URL]` — send HTTP requests and view responses.
* `wget [URL]` — download files from the web.

---

## 🌍 Common Network Ports
* `20/21` — FTP (File Transfer Protocol)
* `22` — SSH (Secure Shell)
* `23` — Telnet
* `25` — SMTP (Email Sending)
* `53` — DNS (Domain Name System)
* `80` — HTTP
* `110` — POP3 (Email Receiving)
* `143` — IMAP (Email Receiving)
* `443` — HTTPS
* `3389` — RDP (Remote Desktop Protocol)

---

## 📖 Basic Networking Terms
* **IP Address** — unique address assigned to a device on a network.
* **MAC Address** — physical address of a network interface.
* **Subnet Mask** — defines the network and host portions of an IP address.
* **Gateway** — device that connects different networks.
* **DNS** — translates domain names into IP addresses.
* **DHCP** — automatically assigns IP addresses to devices.
* **TCP** — reliable, connection-oriented protocol.
* **UDP** — fast, connectionless protocol.

---

## 🔍 Useful Tools
* `nmap` — scan hosts and discover open ports.
* `tcpdump` — capture and analyze network traffic.
* `Wireshark` — graphical packet analyzer.
* `nc` (Netcat) — read/write network connections.
