# 🖧 MAC Address

## 📖 Overview

A **MAC (Media Access Control) address** is a unique hardware identifier assigned to a network interface.

Unlike an IP address, a MAC address identifies the **network adapter itself** and is primarily used for communication within a local network (LAN).

---

## 🎯 Why Is It Important?

MAC addresses enable devices on the same local network to identify one another.

They are essential for:

- Ethernet communication.
- Switching.
- ARP.
- Device identification.
- Network troubleshooting.

Cybersecurity professionals also encounter MAC addresses during network analysis and penetration testing.

---

## ⚙️ How It Works

Every network interface card (NIC) has its own MAC address.

When two devices communicate within the same LAN:

1. The sender determines the destination IP address.
2. ARP resolves the destination MAC address.
3. An Ethernet frame is created.
4. The frame is delivered using MAC addresses.
5. Switches forward frames based on MAC addresses.

Unlike IP addresses, MAC addresses are not used for routing traffic across the Internet.

---

## 🧩 Key Concepts

### MAC Address Structure

A MAC address:

- Is **48 bits** long.
- Contains **12 hexadecimal characters**.
- Is divided into **6 pairs**.

Example:

```text
A4:C3:F0:85:AC:2D
```

| Part | Description |
|------|-------------|
| First 24 bits | Organizationally Unique Identifier (OUI) |
| Last 24 bits | Device identifier |

---

### MAC Spoofing

Although manufacturers assign MAC addresses, operating systems allow them to be changed temporarily.

This process is known as **MAC spoofing**.

Common uses include:

- Privacy protection.
- Penetration testing.
- Bypassing MAC filtering.
- Device impersonation.

---

### MAC Filtering

Some networks allow access only to approved MAC addresses.

Examples include:

- Home Wi-Fi routers
- Hotels
- Cafés
- Enterprise guest networks

Because MAC addresses can be spoofed, MAC filtering should not be considered a strong security mechanism.

---

## 🌍 Real-World Examples

When a laptop communicates with a printer on the same LAN:

- IP addresses identify the destination.
- MAC addresses deliver the Ethernet frame to the correct device.

---

## 🔒 Security Notes

- MAC addresses can be spoofed.
- MAC filtering alone is insufficient for authentication.
- Attackers often change MAC addresses during wireless penetration testing.
- Switches rely on MAC addresses to forward Ethernet frames.

---

## 💻 Practical Examples

### Linux

```bash
ip a
```

Example:

```text
link/ether 08:00:27:AB:CD:EF
```

---

### Windows

```cmd
getmac
```

or

```cmd
ipconfig /all
```

---

## ⚠️ Common Mistakes

- Assuming MAC addresses cannot be changed.
- Confusing MAC addresses with IP addresses.
- Believing MAC filtering provides strong security.
- Thinking MAC addresses are used on the Internet.

---

## 📝 Key Takeaways

- A MAC address uniquely identifies a network interface.
- MAC addresses operate at Layer 2 of the OSI model.
- They are used for communication within a local network.
- MAC addresses can be spoofed.
- Switches forward Ethernet frames using MAC addresses.
