# 📦 Transmission Control Protocol (TCP)

## 📖 Overview

**TCP (Transmission Control Protocol)** is one of the core protocols of the TCP/IP suite.

It provides **reliable, connection-oriented communication** between devices on a network.

Unlike UDP, TCP ensures that:

- Data arrives successfully.
- Packets arrive in the correct order.
- Corrupted or lost packets are retransmitted.
- Duplicate packets are discarded.

Because of these features, TCP is widely used by applications that require reliable communication.

---

## 🎯 Why Is It Important?

TCP is one of the most commonly used protocols on the Internet.

It is responsible for communication used by services such as:

- HTTP / HTTPS
- SSH
- FTP
- SMTP
- IMAP
- POP3

As a cybersecurity professional, understanding TCP is essential for:

- Packet analysis
- Network troubleshooting
- Firewall configuration
- Port scanning
- Understanding attacks such as SYN Flood

---

## ⚙️ How TCP Works

Unlike UDP, TCP is **connection-oriented**.

Before data can be transmitted, the client and server must establish a connection.

During communication TCP guarantees:

- Reliable delivery
- Correct packet order
- Error checking
- Flow control
- Congestion control

After communication is complete, the connection is properly closed.

---

# 🧩 TCP/IP Model

TCP operates at the **Transport Layer** of the TCP/IP model.

| Layer | Responsibility |
|---------|---------------|
| Application | User applications |
| Transport | Reliable communication (TCP/UDP) |
| Internet | Routing (IP) |
| Network Interface | Physical network communication |

As data travels through these layers, **encapsulation** occurs.

Each layer adds its own header before sending the packet.

The receiving device removes these headers in reverse order (decapsulation).

---

# 🤝 TCP Three-Way Handshake

Before any data can be exchanged, TCP establishes a connection using the **Three-Way Handshake**.

The purpose of this process is to synchronize both devices and agree on sequence numbers.

### Step 1 — SYN

The client sends a **SYN** packet.

> "I'd like to establish a connection."

---

### Step 2 — SYN/ACK

The server replies with **SYN/ACK**.

> "Connection accepted. I acknowledge your request."

---

### Step 3 — ACK

The client sends **ACK**.

> "Connection established."

Both devices can now exchange data.

```
Client                         Server

SYN -------------------------->
      <---------------- SYN/ACK
ACK -------------------------->
```

---

# 🔢 Sequence Numbers

Every TCP connection begins with a random **Initial Sequence Number (ISN)**.

Example:

```
Client ISN = 1500
Server ISN = 8000
```

Each transmitted byte increments the sequence number.

Example:

```
Packet 1 → Sequence 1500

Packet 2 → Sequence 1501

Packet 3 → Sequence 1502
```

Acknowledgement numbers tell the sender which packet should be sent next.

This mechanism allows TCP to:

- Detect missing packets
- Detect duplicate packets
- Reassemble packets in the correct order

---

# 📋 Important TCP Headers

| Header | Purpose |
|---------|---------|
| Source Port | Sender's port number |
| Destination Port | Receiver's port number |
| Source IP | Sender's IP address |
| Destination IP | Receiver's IP address |
| Sequence Number | Maintains packet order |
| Acknowledgement Number | Confirms received data |
| Checksum | Detects transmission errors |
| Flags | Controls TCP connection |
| Data | Actual transmitted information |

---

# 🚩 TCP Flags

TCP uses several control flags.

| Flag | Purpose |
|------|----------|
| SYN | Start a connection |
| ACK | Acknowledge received data |
| FIN | Gracefully close a connection |
| RST | Immediately terminate a connection |
| PSH | Immediately deliver data to the application |
| URG | Indicates urgent data |

---

# 📤 Data Transmission

After the handshake is complete, the client and server exchange data.

Each packet contains:

- Sequence Number
- Acknowledgement Number
- Data

If a packet is lost, TCP automatically retransmits it.

---

# 🔚 Closing a TCP Connection

When communication finishes, TCP closes the connection gracefully.

The process is known as the **Four-Way Handshake**.

### Step 1

Client sends **FIN**.

> "I'm finished sending data."

---

### Step 2

Server replies **ACK**.

> "I received your FIN."

---

### Step 3

Server sends its own **FIN**.

> "I'm also finished."

---

### Step 4

Client replies **ACK**.

The connection is now closed.

```
Client                         Server

FIN -------------------------->
      <---------------- ACK
      <---------------- FIN
ACK -------------------------->
```

---

# ✅ Advantages

- Reliable communication
- Packet ordering
- Error detection
- Packet retransmission
- Flow control
- Congestion control

---

# ❌ Disadvantages

- Slower than UDP
- Requires connection establishment
- More protocol overhead
- Higher CPU usage
- Increased latency

---

## 🌍 Real-World Examples

### Opening a Website

When visiting an HTTPS website:

1. TCP establishes a connection.
2. TLS negotiates encryption.
3. HTTP requests are exchanged.
4. TCP closes the connection.

---

### Downloading a File

TCP guarantees that every byte of the file arrives correctly and in the proper order.

If one packet is lost, it is retransmitted automatically.

---

## 🔒 Security Notes

TCP is commonly targeted by network attacks.

Examples include:

- SYN Flood
- TCP Session Hijacking
- TCP Reset (RST) Attack
- Port Scanning
- TCP Sequence Prediction

Understanding the TCP handshake is essential when analyzing attacks with tools like Wireshark or tcpdump.

---

## 💻 Practical Examples

Display active TCP connections:

### Windows

```cmd
netstat -an
```

### Linux

```bash
ss -t
```

Capture TCP traffic:

```bash
tcpdump tcp
```

---

## ⚠️ Common Mistakes

- Thinking TCP guarantees low latency.
- Confusing TCP with IP.
- Assuming TCP is always faster than UDP.
- Believing TCP only sends data after the handshake (connection establishment still requires packets).
- Forgetting that TCP uses sequence numbers to restore packet order.

---

## 📝 Key Takeaways

- TCP is a reliable, connection-oriented transport protocol.
- TCP establishes communication using the Three-Way Handshake.
- Sequence and acknowledgement numbers ensure correct packet ordering.
- TCP automatically retransmits lost packets.
- Connections are terminated using the Four-Way Handshake.
- TCP prioritizes reliability over speed.
