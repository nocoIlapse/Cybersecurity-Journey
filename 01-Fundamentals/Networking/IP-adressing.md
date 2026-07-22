# 🌐 IP & MAC Addressing

## 📖 Overview

Every device connected to a network has two important identifiers:

- **IP Address** — a logical address used to identify a device on a network and route traffic between networks.
- **MAC Address** — a physical hardware address assigned to a network interface, used for communication within a local network (LAN).

Although both identify devices, they serve different purposes and operate at different layers of the OSI model.

---

## 🎯 Why Is It Important?

Understanding IP and MAC addresses is essential for networking and cybersecurity because they are used in almost every network communication.

As a cybersecurity professional, you will use them to:

- Troubleshoot network connectivity.
- Analyze network traffic.
- Perform network reconnaissance.
- Identify hosts on a network.
- Understand attacks such as ARP spoofing and MAC spoofing.

---

# 🌐 IP Address

## What is an IP Address?

An **IP (Internet Protocol) address** is a logical identifier assigned to a device connected to a network.

Its primary purpose is to uniquely identify a device and allow data to be routed between different networks.

Unlike a MAC address, an IP address **can change**. It may be assigned manually (Static IP) or automatically by a DHCP server (Dynamic IP).

---

## IPv4 Address Structure

An IPv4 address consists of **32 bits**, divided into **four octets**.

Example:

```text
192.168.1.10
```

Each octet:

- Contains values from **0 to 255**
- Represents **8 bits**
- Four octets together form a **32-bit** address

---

## Public vs Private IP Addresses

| Type | Description |
|------|-------------|
| **Public IP** | Accessible from the Internet and used to communicate with external networks. |
| **Private IP** | Used only inside local networks (LANs) and cannot be reached directly from the Internet. |

Most home and office networks use **private IP addresses**, while the router communicates with the Internet using a **public IP address**.

---

## Common Private IPv4 Ranges

| Range | CIDR |
|--------|------|
| `10.0.0.0 – 10.255.255.255` | `/8` |
| `172.16.0.0 – 172.31.255.255` | `/12` |
| `192.168.0.0 – 192.168.255.255` | `/16` |

---

# 🖧 MAC Address

## What is a MAC Address?

A **MAC (Media Access Control) address** is a unique hardware identifier assigned to a network interface by the manufacturer.

Every network interface (Ethernet, Wi-Fi, etc.) has its own MAC address.

Unlike an IP address, a MAC address identifies the **network adapter itself**, not its location on a network.

---

## MAC Address Structure

A MAC address:

- Is **48 bits** long.
- Consists of **12 hexadecimal characters**.
- Is divided into **6 pairs** separated by colons (`:`) or hyphens (`-`).

Example:

```text
A4:C3:F0:85:AC:2D
```

| Part | Description |
|------|-------------|
| First 6 hexadecimal characters | Organizationally Unique Identifier (OUI) — identifies the manufacturer |
| Last 6 hexadecimal characters | Unique identifier assigned to the network interface |

---

## MAC Spoofing

Although MAC addresses are assigned by manufacturers, most operating systems allow them to be changed temporarily.

This process is known as **MAC spoofing**.

Common uses include:

- Privacy protection.
- Penetration testing.
- Bypassing MAC-based access control.
- Impersonating another device on the network.

---

## MAC Filtering

Some networks restrict access based on MAC addresses.

Examples include:

- Home Wi-Fi routers
- Hotels
- Cafés
- Public Wi-Fi hotspots

However, **MAC filtering should not be considered a strong security mechanism**, since MAC addresses can be spoofed.

---

# ⚙️ How IP and MAC Work Together

When a device sends data over a network, both addresses are used.

1. The application creates data to send.
2. The operating system determines the destination IP address.
3. If the destination is on the local network, the sender discovers the destination MAC address (typically using ARP).
4. The frame is sent using the destination MAC address.
5. Routers use the IP address to forward the packet toward its destination.

```text
Application
      │
      ▼
Destination IP Address
      │
      ▼
Find Destination MAC Address
      │
      ▼
Ethernet Frame
      │
      ▼
Local Network
```

---

## 🔒 Security Notes

From a cybersecurity perspective:

- MAC addresses can be spoofed and should not be used as the only authentication mechanism.
- Public IP addresses are exposed to the Internet and may become attack targets.
- Private IP addresses are typically protected by Network Address Translation (NAT), but they are still vulnerable to attacks from inside the local network.

---

## 💻 Practical Examples

Display network interfaces, IP addresses, and MAC addresses on Linux:

```bash
ip a
```

Example output:

```text
2: eth0
    link/ether 08:00:27:AB:CD:EF
    inet 192.168.1.15/24
```

- `link/ether` → MAC Address
- `inet` → IPv4 Address

---

## ⚠️ Common Mistakes

- Confusing MAC addresses with IP addresses.
- Assuming MAC addresses can never be changed.
- Believing MAC filtering provides strong security.
- Thinking private IP addresses are accessible directly from the Internet.

---

## 📝 Key Takeaways

- An IP address identifies a device on a network and enables routing between networks.
- A MAC address uniquely identifies a network interface within a local network.
- IP addresses can change, while MAC addresses are typically permanent but can be spoofed.
- Private IP addresses are used inside local networks, while public IP addresses communicate over the Internet.
- MAC addresses operate at Layer 2 of the OSI model, while IP addresses operate at Layer 3.
