# 📡 Dynamic Host Configuration Protocol (DHCP)

## 📖 Overview

**DHCP (Dynamic Host Configuration Protocol)** is a network protocol that automatically assigns IP configuration to devices connected to a network.

Instead of manually configuring every device, a DHCP server provides the necessary network settings, allowing devices to communicate with other systems immediately after joining the network.

---

## 🎯 Why Is It Important?

Without DHCP, every device would need to be configured manually with:

- An IP address
- A Subnet Mask
- A Default Gateway
- DNS server addresses

This process is impractical in networks with many devices and increases the risk of configuration errors or duplicate IP addresses.

DHCP automates this process, making network administration faster and more reliable.

---

## ⚙️ How DHCP Works

When a device connects to a network without an IP address, it communicates with a DHCP server through a four-step process known as **DORA**.

### 1. DHCP Discover

The client broadcasts a **DHCP Discover** message to locate available DHCP servers.

> "Is there a DHCP server on this network?"

---

### 2. DHCP Offer

A DHCP server responds with a **DHCP Offer**, suggesting an available IP address and other network settings.

> "You can use this IP address."

---

### 3. DHCP Request

The client sends a **DHCP Request**, informing the server that it wants to use the offered IP address.

> "I accept this IP address."

---

### 4. DHCP Acknowledgment (ACK)

The DHCP server sends a **DHCP ACK**, confirming that the IP address has been assigned.

The client can now communicate on the network.

---

### DHCP Process (DORA)

```text
Client                         DHCP Server
   |                                 |
   | ---- DHCP Discover -----------> |
   |                                 |
   | <------ DHCP Offer ------------ |
   |                                 |
   | ---- DHCP Request ------------> |
   |                                 |
   | <------- DHCP ACK ------------- |
   |                                 |
```

---

## 🧩 Key Concepts

| Term | Description |
|------|-------------|
| **DHCP Server** | Assigns IP addresses and network configuration to clients. |
| **DHCP Client** | A device requesting network configuration. |
| **Dynamic IP Address** | An IP address assigned automatically by DHCP. |
| **Static IP Address** | An IP address configured manually. |
| **Lease Time** | The period for which an IP address is assigned to a client before renewal is required. |

---

## 🌍 Real-World Examples

### Home Network

When you connect your laptop to your home Wi-Fi, the router (acting as a DHCP server) automatically assigns:

- IP address
- Subnet mask
- Default gateway
- DNS servers

No manual configuration is required.

---

### Enterprise Network

In large organizations, hundreds or thousands of devices receive network settings automatically from centralized DHCP servers.

This simplifies network management and reduces administrative overhead.

---

## 🔒 Security Notes

- DHCP itself does **not authenticate** clients.
- A **Rogue DHCP Server** can distribute incorrect network settings, redirecting traffic to an attacker.
- DHCP starvation attacks attempt to exhaust the pool of available IP addresses, preventing legitimate devices from obtaining one.

---

## 💻 Practical Examples

### Windows

Display the current DHCP-assigned configuration:

```cmd
ipconfig /all
```

Look for:

```text
DHCP Enabled . . . . . : Yes
```

---

### Linux

Display the current IP address:

```bash
ip a
```

Some distributions also allow checking lease information:

```bash
cat /var/lib/dhcp/dhclient.leases
```

---

## ⚠️ Common Mistakes

- Assuming DHCP only assigns an IP address.
- Confusing DHCP with DNS.
- Believing a dynamically assigned IP address never changes.
- Assuming DHCP is secure against malicious servers.

---

## 📝 Key Takeaways

- DHCP automatically assigns network configuration to devices.
- It eliminates the need for manual IP configuration.
- The DHCP process consists of four steps: **Discover → Offer → Request → ACK (DORA)**.
- DHCP assigns more than just an IP address, including the subnet mask, default gateway, and DNS servers.
- Understanding DHCP is essential for networking, troubleshooting, and cybersecurity.
