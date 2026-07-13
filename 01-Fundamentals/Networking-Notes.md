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

## 🌐 HTTP Methods

HTTP uses **methods** (also called **verbs**) to specify what action the client wants to perform on a resource.

| Method | Description | Example |
|---------|-------------|---------|
| `GET` | Retrieve data from the server. | Open a web page or get a list of users. |
| `POST` | Send data to create a new resource. | Register a new account or submit a form. |
| `PUT` | Replace an existing resource completely. | Update all information about a user. |
| `PATCH` | Update part of an existing resource. | Change only a user's password or email. |
| `DELETE` | Remove a resource from the server. | Delete a user or a file. |
| `HEAD` | Retrieve only the response headers. | Check if a resource exists without downloading it. |
| `OPTIONS` | Show which HTTP methods are supported. | Check available API methods. |
| `CONNECT` | Establish a tunnel to the server (commonly for HTTPS via a proxy). | HTTPS proxy connection. |
| `TRACE` | Echo the received request for debugging purposes. | HTTP request diagnostics. |

---

## 🖥️ Virtualization & Infrastructure

* **Virtualization** — technology that allows one physical computer to run multiple independent virtual machines.
* **Hypervisor** — software that creates, manages, and runs virtual machines.
* **Virtual Machine (VM)** — a complete virtual computer with its own operating system, running on a host machine.
* **Container** — a lightweight isolated environment for running applications while sharing the host operating system.
* **Container Image** — a reusable template containing everything needed to create a container.
* **Network Port** — a numbered communication endpoint that applications use to send and receive network traffic.

---

## ☁️ Cloud Service Models

Cloud computing provides different levels of managed services depending on how much control you need.

| Model | Description | You Manage | Provider Manages |
|--------|-------------|------------|------------------|
| **IaaS** (Infrastructure as a Service) | Rent virtual servers, storage, and networking resources. | Operating system, applications, data. | Physical hardware, networking, virtualization. |
| **PaaS** (Platform as a Service) | Develop and deploy applications without managing servers. | Applications and data. | Infrastructure, operating system, runtime environment. |
| **SaaS** (Software as a Service) | Use a complete application over the Internet. | Only your data and application settings. | Everything else. |

### 💡 Examples

* **IaaS** — AWS EC2, Microsoft Azure Virtual Machines, Google Compute Engine.
* **PaaS** — Heroku, Google App Engine, Azure App Service.
* **SaaS** — Gmail, Zoom, Microsoft 365, Dropbox.

---

## 🔍 Useful Tools
* `nmap` — scan hosts and discover open ports.
* `tcpdump` — capture and analyze network traffic.
* `Wireshark` — graphical packet analyzer.
* `nc` (Netcat) — read/write network connections.
