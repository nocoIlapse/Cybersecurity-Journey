# 🌐 OSI Model (Open Systems Interconnection)

## 📖 Overview

The **OSI (Open Systems Interconnection) Model** is a conceptual framework that describes how devices communicate over a network.

It divides network communication into **seven layers**, each responsible for a specific part of the communication process.

By separating networking into layers, the OSI model allows devices from different manufacturers and operating systems to communicate using standardized protocols.

Although modern networks primarily use the **TCP/IP model**, the OSI model remains the standard for learning, troubleshooting, and understanding how networks operate.

---

## 🎯 Why Is It Important?

The OSI model helps network engineers and cybersecurity professionals understand **how data moves across a network**.

It is widely used for:

- Understanding network communication.
- Troubleshooting connectivity issues.
- Learning networking protocols.
- Identifying which layer an attack targets.
- Analyzing network traffic.

Most networking concepts, protocols, and security tools can be mapped to one or more OSI layers.

---

## ⚙️ How It Works

When data is sent from one device to another, it passes through all seven OSI layers.

Each layer performs a specific task before passing the data to the next layer.

On the receiving device, the process happens in reverse.

This process is called **encapsulation**.

```text
Sender                          Receiver

Application  ───────────────►  Application
Presentation ───────────────►  Presentation
Session      ───────────────►  Session
Transport    ───────────────►  Transport
Network      ───────────────►  Network
Data Link    ───────────────►  Data Link
Physical     ───────────────►  Physical
```

As data travels down the stack, each layer adds its own information (called a **header**, and sometimes a trailer).

When the receiving device gets the data, each layer removes its corresponding header until the original application data is recovered.

---

# 🧩 The Seven OSI Layers

| Layer | Name | Main Responsibility |
|------:|------|---------------------|
| **7** | Application | Provides network services to applications. |
| **6** | Presentation | Formats, encrypts, and compresses data. |
| **5** | Session | Establishes, manages, and terminates communication sessions. |
| **4** | Transport | Ensures reliable data delivery and error recovery. |
| **3** | Network | Routes packets between different networks. |
| **2** | Data Link | Transfers frames within a local network using MAC addresses. |
| **1** | Physical | Transmits raw bits through physical media. |

---

## Layer 7 — Application

The Application layer provides network services directly to end-user applications.

Examples:

- HTTP
- HTTPS
- FTP
- SMTP
- DNS

This layer is where users interact with network services.

---

## Layer 6 — Presentation

Responsible for translating data into a format that applications can understand.

Functions include:

- Encryption
- Decryption
- Compression
- Character encoding

Example:

HTTPS uses encryption before data is transmitted.

---

## Layer 5 — Session

Responsible for creating, maintaining, and terminating communication sessions.

Examples include:

- Authentication sessions
- Remote desktop sessions
- Video conferencing sessions

---

## Layer 4 — Transport

Responsible for reliable communication between devices.

Main functions:

- Segmentation
- Error detection
- Flow control
- Reliability

Common protocols:

- TCP
- UDP

---

## Layer 3 — Network

Responsible for routing packets between different networks.

Main functions:

- Logical addressing
- Routing
- Path selection

Uses:

- IP addresses
- Routers

---

## Layer 2 — Data Link

Responsible for communication inside a local network.

Main functions:

- MAC addressing
- Error detection
- Frame delivery

Uses:

- Switches
- Ethernet
- MAC addresses

---

## Layer 1 — Physical

Responsible for transmitting electrical, optical, or wireless signals.

Examples:

- Ethernet cables
- Fiber optic cables
- Wi-Fi radio signals

This layer transmits **bits**, not frames or packets.

---

## 🌍 Real-World Example

Imagine opening a website.

1. Your browser creates an HTTP request (**Layer 7**).
2. The data is encrypted using TLS (**Layer 6**).
3. A communication session is maintained (**Layer 5**).
4. TCP ensures reliable delivery (**Layer 4**).
5. The packet is routed using IP addresses (**Layer 3**).
6. The packet is placed into an Ethernet frame using MAC addresses (**Layer 2**).
7. The bits are transmitted through a network cable or Wi-Fi (**Layer 1**).

---

## 🔒 Security Notes

Many cyberattacks target specific OSI layers.

Examples:

| Layer | Example Attack |
|---------|----------------|
| 7 | SQL Injection, XSS |
| 6 | Weak TLS configuration |
| 5 | Session Hijacking |
| 4 | TCP SYN Flood |
| 3 | IP Spoofing |
| 2 | ARP Spoofing, MAC Flooding |
| 1 | Cable tapping, Physical sabotage |

Understanding the OSI model helps security professionals determine where an attack occurs and which technologies are affected.

---

## 💻 Practical Examples

Capture network traffic using Wireshark.

You can observe:

- Ethernet Frames (Layer 2)
- IP Packets (Layer 3)
- TCP Segments (Layer 4)
- HTTP Requests (Layer 7)

This demonstrates how multiple OSI layers work together during communication.

---

## ⚠️ Common Mistakes

- Thinking the OSI model is a protocol.
- Assuming all protocols belong to only one layer.
- Confusing the OSI model with the TCP/IP model.
- Believing the Internet directly "uses OSI" instead of TCP/IP.

---

## 📝 Key Takeaways

- The OSI model is a conceptual framework for understanding network communication.
- It consists of **seven layers**, each with a specific responsibility.
- Data moves from Layer 7 to Layer 1 when sent and from Layer 1 to Layer 7 when received.
- During transmission, each layer adds its own information through a process called **encapsulation**.
- Understanding the OSI model is essential for networking, troubleshooting, and cybersecurity.
