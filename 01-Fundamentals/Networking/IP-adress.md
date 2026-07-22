# 🌐 IP Addressing

## 📖 Overview

An **IP (Internet Protocol) address** is a logical identifier assigned to a device connected to a network.

It allows devices to communicate across networks and enables routers to determine where data should be delivered.

Unlike a MAC address, an IP address identifies a device's **location on a network**, not the hardware itself.

---

## 🎯 Why Is It Important?

IP addresses are fundamental to modern networking.

Without IP addressing, devices would be unable to communicate across different networks, including the Internet.

As a cybersecurity professional, understanding IP addressing is essential for:

- Troubleshooting network connectivity.
- Performing network reconnaissance.
- Configuring network devices.
- Analyzing network traffic.
- Understanding routing and network segmentation.

---

## ⚙️ How It Works

Every device connected to a network must have an IP address.

When a device sends data:

1. The operating system creates an IP packet.
2. The packet contains the source and destination IP addresses.
3. Routers examine the destination IP address.
4. The packet is forwarded through one or more networks until it reaches its destination.

Unlike MAC addresses, IP addresses may change depending on the network a device connects to.

---

## 🧩 Key Concepts

### IPv4 Address Structure

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

### Public vs Private IP Addresses

| Type | Description |
|------|-------------|
| **Public IP** | Accessible from the Internet and used for communication between external networks. |
| **Private IP** | Used within local networks (LANs) and cannot be accessed directly from the Internet. |

Most home and office devices use **private IP addresses**, while the router communicates with the Internet using a **public IP address**.

---

### Common Private IPv4 Ranges

| Range | CIDR |
|--------|------|
| `10.0.0.0 – 10.255.255.255` | `/8` |
| `172.16.0.0 – 172.31.255.255` | `/12` |
| `192.168.0.0 – 192.168.255.255` | `/16` |

---

## 🌍 Real-World Examples

### Home Network

A laptop connects to a Wi-Fi router and automatically receives:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

using DHCP.

---

### Corporate Network

A workstation receives a private IP address from the company's DHCP server, allowing it to communicate with other devices inside the organization while accessing the Internet through the company's public IP address.

---

## 🔒 Security Notes

- Public IP addresses are directly exposed to the Internet and may become attack targets.
- Private IP addresses are commonly protected by Network Address Translation (NAT).
- IP addresses can be spoofed in certain attacks, although TCP communication makes successful spoofing more difficult.
- Knowing a target's IP address is often the first step in network reconnaissance.

---

## 💻 Practical Examples

### Linux

```bash
ip a
```

---

### Windows

```cmd
ipconfig
```

---

## ⚠️ Common Mistakes

- Confusing private and public IP addresses.
- Assuming an IP address uniquely identifies a physical device.
- Believing an IP address never changes.
- Confusing IP addresses with MAC addresses.

---

## 📝 Key Takeaways

- An IP address is a logical identifier used for communication between networks.
- IPv4 addresses consist of 32 bits.
- IP addresses may be static or dynamically assigned.
- Public IP addresses communicate over the Internet, while private IP addresses are used inside local networks.
- Routers forward traffic based on IP addresses.
