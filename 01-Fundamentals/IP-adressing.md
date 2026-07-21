# 🌐 IP & MAC Addressing

## 🌐 IP Addressing

### What is an IP Address?

An **IP (Internet Protocol) address** is a unique identifier assigned to a device on a network. It allows devices to communicate with each other.

📌 An IP address identifies a device on a network, but it is **not permanently tied** to that device and can change over time.

---

### IPv4 Address Structure

An IPv4 address consists of **four octets** separated by dots.

Example:

```text
192.168.1.10
```

Each octet:

- Contains a value from **0 to 255**
- Represents **8 bits**
- Together form a **32-bit** address.

---

### Public vs Private IP Addresses

| Type | Description |
|------|-------------|
| **Public IP** | Used to identify a device on the Internet. |
| **Private IP** | Used to identify a device within a local network (LAN). |

Private IP addresses are **not directly accessible from the Internet**.

---

### Common Private IPv4 Ranges

| Range | CIDR |
|--------|------|
| `10.0.0.0 - 10.255.255.255` | `10.0.0.0/8` |
| `172.16.0.0 - 172.31.255.255` | `172.16.0.0/12` |
| `192.168.0.0 - 192.168.255.255` | `192.168.0.0/16` |

---

## 🖧 MAC Addresses

### What is a MAC Address?

A **MAC (Media Access Control) address** is a unique hardware identifier assigned to a network interface by the manufacturer.

📌 Unlike an IP address, a MAC address identifies the **network adapter**, not the network location.

---

### MAC Address Structure

A MAC address:

- Consists of **12 hexadecimal characters**.
- Is divided into **6 pairs** separated by colons (`:`) or hyphens (`-`).
- Is **48 bits** long.

Example:

```text
a4:c3:f0:85:ac:2d
```

| Part | Description |
|------|-------------|
| First 6 characters | Manufacturer Identifier (OUI) |
| Last 6 characters | Unique identifier assigned by the manufacturer |

---

### MAC Address Spoofing

**MAC spoofing** is the process of changing or faking a device's MAC address.

📌 Attackers may spoof a MAC address to impersonate another device on the network.

Possible uses:

- Bypass MAC-based access control.
- Impersonate trusted devices.
- Perform penetration testing.
- Protect privacy on public networks.

---

### MAC Filtering

Some networks allow or deny access based on MAC addresses.

Common examples:

- Home Wi-Fi routers
- Hotels
- Cafés
- Public Wi-Fi hotspots

⚠️ MAC filtering **should not be considered a strong security mechanism**, since MAC addresses can be spoofed.

---

## 🔑 Key Differences

| IP Address | MAC Address |
|------------|-------------|
| Logical address | Physical hardware address |
| Can change | Usually remains the same |
| Used for routing between networks | Used for communication within a local network |
| Assigned manually or by DHCP | Assigned by the manufacturer |
| IPv4 = 32 bits | 48 bits |

---
