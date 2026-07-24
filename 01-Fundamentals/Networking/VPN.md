# 🔒 Virtual Private Network (VPN)

## 📖 Overview

A **Virtual Private Network (VPN)** is a technology that creates a **secure, encrypted connection (tunnel)** between devices over the Internet.

Although the Internet is a public network, a VPN allows devices to communicate as if they were connected to the same private network.

This secure connection is commonly referred to as a **VPN tunnel**.

---

## 🎯 Why Is It Important?

VPNs are widely used by individuals and organizations to provide secure communication over untrusted networks.

Common use cases include:

- Secure remote access to corporate networks.
- Connecting multiple office locations.
- Protecting data on public Wi-Fi networks.
- Encrypting Internet traffic.
- Improving online privacy.
- Accessing internal company resources remotely.

Cybersecurity professionals regularly use VPNs to securely access internal systems, penetration testing labs, and cloud environments.

---

## ⚙️ How VPN Works

Normally, when you connect to a website, your traffic travels across the Internet in plain routing (although application protocols such as HTTPS may encrypt the content).

A VPN adds another layer of protection by creating an encrypted tunnel between your device and the VPN server.

```text
Without VPN

Your Device
      │
      ▼
   Internet
      │
      ▼
 Destination
```

```text
With VPN

Your Device
      │
Encrypted Tunnel
      │
      ▼
 VPN Server
      │
      ▼
 Destination
```

Anyone observing the network can see that you are connected to a VPN server, but they cannot easily inspect the encrypted traffic inside the tunnel.

---

## 🧩 Key Concepts

### VPN Tunnel

A VPN tunnel is an encrypted communication channel between two endpoints.

Only devices participating in the VPN can decrypt and read the transmitted data.

---

### Encryption

VPNs encrypt data before it leaves your device.

This protects sensitive information from attackers who may be monitoring the network.

Encryption is especially important when using:

- Public Wi-Fi
- Airport networks
- Hotels
- Cafés

---

### Authentication

Before a VPN connection is established, both devices authenticate each other.

Authentication may use:

- Username and password
- Digital certificates
- Cryptographic keys
- Multi-factor authentication (MFA)

Only authorized users are allowed to join the VPN.

---

## 🌍 Real-World Examples

### Remote Employee

An employee working from home connects to the company's VPN.

Once connected, they can securely access:

- File servers
- Internal websites
- Databases
- Remote desktops

as if they were physically in the office.

---

### Site-to-Site VPN

Two company offices in different cities establish a permanent VPN connection.

Employees in both offices can access shared resources securely over the Internet.

---

### TryHackMe VPN

TryHackMe uses a VPN to connect your computer to vulnerable lab machines.

This approach provides several benefits:

- Secure access to lab environments.
- Lab machines are not directly exposed to the Internet.
- Your ISP only sees encrypted VPN traffic.
- Attack traffic remains inside the VPN tunnel.

---

## 🔒 Security Notes

Although VPNs improve privacy and security, they do **not** guarantee complete anonymity.

Keep in mind:

- Your VPN provider may log your activity.
- VPNs do not protect against malware.
- VPNs do not automatically make browsing anonymous.
- HTTPS should still be used even when connected to a VPN.

A VPN protects **data in transit**, not the endpoint itself.

---

## ⚖️ Advantages

- Encrypts Internet traffic.
- Protects users on public Wi-Fi.
- Enables secure remote access.
- Connects geographically separated networks.
- Helps reduce network eavesdropping.

---

## ❌ Disadvantages

- Can reduce Internet speed because of encryption.
- Requires trust in the VPN provider.
- Some VPN protocols are outdated and insecure.
- Does not prevent phishing or malware attacks.
- Misconfigured VPNs can expose sensitive information.

---

# 📚 Common VPN Technologies

## PPP (Point-to-Point Protocol)

PPP provides authentication and encryption mechanisms for point-to-point communication.

It cannot route traffic across the Internet by itself and is primarily used together with tunneling protocols.

---

## PPTP (Point-to-Point Tunneling Protocol)

PPTP encapsulates PPP traffic and allows it to travel across IP networks.

Advantages:

- Easy to configure.
- Supported by many operating systems.

Disadvantages:

- Uses outdated encryption.
- Considered insecure for modern environments.
- Should generally be avoided in favor of newer VPN protocols.

---

## IPsec (Internet Protocol Security)

IPsec secures communication at the Internet (Network) layer by encrypting IP packets.

Advantages:

- Strong encryption.
- Widely supported.
- Commonly used for Site-to-Site VPNs and enterprise networks.

Disadvantages:

- More complex to configure.
- Troubleshooting can be difficult.

---

## 💻 Practical Examples

### Linux

Display VPN interfaces:

```bash
ip a
```

Common VPN interfaces include:

```text
tun0
tap0
wg0
```

---

### Windows

Display network adapters:

```cmd
ipconfig /all
```

VPN adapters usually appear as additional network interfaces.

---

## ⚠️ Common Mistakes

- Thinking a VPN makes you completely anonymous.
- Assuming VPNs protect against malware.
- Believing VPNs replace HTTPS.
- Trusting every VPN provider equally.
- Using outdated protocols such as PPTP for sensitive communication.

---

## 📝 Key Takeaways

- A VPN creates an encrypted tunnel over the Internet.
- VPNs protect data in transit between connected devices.
- They are commonly used for secure remote access and connecting private networks.
- VPNs improve privacy but do not guarantee anonymity.
- Modern VPN deployments commonly use IPsec, OpenVPN, or WireGuard rather than older protocols such as PPTP.
