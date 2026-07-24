# 📡 User Datagram Protocol (UDP)

## 📖 Overview

**UDP (User Datagram Protocol)** is a connectionless transport protocol in the TCP/IP suite.

Unlike TCP, UDP **does not establish a connection before sending data** and does not guarantee that packets will arrive, arrive in order, or arrive only once.

Instead, UDP focuses on **speed and low latency**, making it ideal for applications where occasional packet loss is acceptable.

---

## 🎯 Why Is It Important?

UDP is designed for applications that require fast communication rather than guaranteed delivery.

It is commonly used by:

- DNS
- DHCP
- VoIP (Voice over IP)
- Online gaming
- Live video streaming
- Video conferencing

As a cybersecurity professional, understanding UDP is essential for:

- Network troubleshooting
- Packet analysis
- Firewall configuration
- Understanding UDP-based attacks
- Enumerating UDP services

---

## ⚙️ How UDP Works

Unlike TCP, UDP is **connectionless**.

There is:

- ❌ No Three-Way Handshake
- ❌ No acknowledgement (ACK)
- ❌ No retransmission
- ❌ No packet ordering

The sender simply transmits packets to the destination.

If a packet is lost, UDP does not attempt to recover it.

```text
Client                         Server

Request ----------------------->

               Responce <--------

               Responce <--------

               Responce <--------
```

The sender has no way of knowing whether the packets successfully reached the destination.

---

# 🧩 UDP in the TCP/IP Model

UDP operates at the **Transport Layer** of the TCP/IP model.

| Layer | Responsibility |
|---------|---------------|
| Application | User applications |
| Transport | Communication (TCP / UDP) |
| Internet | Routing using IP |
| Network Interface | Physical network communication |

Like TCP, UDP relies on **encapsulation**, where each layer adds its own header before transmission.

---

# 📋 UDP Packet Headers

UDP packets are much simpler than TCP packets.

| Header | Purpose |
|---------|---------|
| Source IP | Sender's IP address |
| Destination IP | Receiver's IP address |
| Source Port | Sender's port |
| Destination Port | Receiver's port |
| Length | Total size of the UDP datagram |
| Checksum | Detects transmission errors |
| Data | Actual transmitted information |

> **Note:** In IPv4, the **Time To Live (TTL)** field belongs to the **IP header**, not the UDP header. The IP layer decrements TTL at each router to prevent packets from circulating indefinitely.

---

# 📤 Data Transmission

UDP immediately sends data without first creating a connection.

```
Application
      │
      ▼
UDP Datagram
      │
      ▼
IP Packet
      │
      ▼
Network
```

If packets are:

- Lost
- Duplicated
- Delayed
- Arrive out of order

UDP does nothing to correct these issues.

If reliability is required, the application itself must handle it.

---

# ⚖️ TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection | ✅ Yes | ❌ No |
| Reliable Delivery | ✅ Yes | ❌ No |
| Packet Ordering | ✅ Yes | ❌ No |
| Retransmission | ✅ Yes | ❌ No |
| Error Recovery | ✅ Yes | ❌ No |
| Speed | Slower | Faster |
| Overhead | Higher | Lower |

---

# ✅ Advantages

- Very fast communication.
- Low latency.
- Minimal protocol overhead.
- No connection setup.
- Ideal for real-time applications.

---

# ❌ Disadvantages

- No guarantee that packets arrive.
- No acknowledgement mechanism.
- No packet ordering.
- Lost packets are not retransmitted.
- Applications must implement reliability themselves if required.

---

## 🌍 Real-World Examples

### Online Gaming

Position updates are constantly transmitted.

If one packet is lost, the next update quickly replaces it.

Waiting for retransmission would introduce noticeable lag.

---

### Voice Calls

VoIP applications use UDP because receiving audio slightly late is usually worse than losing a small amount of audio.

---

### DNS

A DNS query typically consists of a single request and a single response.

Using TCP would introduce unnecessary overhead.

---

## 🔒 Security Notes

UDP is frequently abused in network attacks because it is connectionless.

Common examples include:

- UDP Flood
- DNS Amplification
- NTP Amplification
- SSDP Amplification
- Reflection attacks

Unlike TCP, there is no handshake to verify that the sender actually exists.

---

## 💻 Practical Examples

### Display UDP connections (Windows)

```cmd
netstat -an -p udp
```

### Display UDP sockets (Linux)

```bash
ss -u
```

Capture UDP traffic:

```bash
tcpdump udp
```

---

## ⚠️ Common Mistakes

- Thinking UDP is "bad" because it is unreliable.
- Assuming UDP cannot detect transmission errors (it includes a checksum).
- Believing UDP is always better because it is faster.
- Confusing UDP's connectionless nature with a lack of addressing (UDP still uses IP addresses and ports).

---

## 📝 Key Takeaways

- UDP is a connectionless transport protocol.
- It does not establish a connection before sending data.
- UDP prioritizes speed over reliability.
- Lost packets are not retransmitted.
- UDP is widely used for real-time communication such as streaming, gaming, VoIP, and DNS.
