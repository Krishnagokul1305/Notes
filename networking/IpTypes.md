# IP Address Reference Guide

## 🔹 Public vs Private IP Addresses

- **Public IP**: Globally routable, assigned by ISPs, unique across the internet.
- **Private IP**: Used within internal networks (intranet), not routable on the internet.
  - Requires **NAT (Network Address Translation)** to access the internet.
  - Common private IP ranges:
    - **Class A**: 10.0.0.0 - 10.255.255.255
    - **Class B**: 172.16.0.0 - 172.31.255.255
    - **Class C**: 192.168.0.0 - 192.168.255.255

## 🔹 Special Address Ranges

- **Loopback (127.0.0.0/8)**: Used for testing & directing traffic to itself (e.g., `127.0.0.1`).
- **Link-local (169.254.0.0/16)**: Automatically assigned when DHCP fails (APIPA in Windows).
- **Multicast (224.0.0.0 - 239.255.255.255)**: Used for group communication.
- **Broadcast (255.255.255.255)**: Sends data to all devices in a network.
- **Experimental (240.0.0.0 - 255.255.255.254)**: Reserved for future use.

## 🔹 IPv4 Address Classes

| Class | Range                       | Usage                        |
| ----- | --------------------------- | ---------------------------- |
| **A** | 1.0.0.0 - 126.255.255.255   | Large networks (>16M hosts)  |
| **B** | 128.0.0.0 - 191.255.255.255 | Medium networks (~65K hosts) |
| **C** | 192.0.0.0 - 223.255.255.255 | Small networks (254 hosts)   |
| **D** | 224.0.0.0 - 239.255.255.255 | Multicast groups             |
| **E** | 240.0.0.0 - 255.255.255.254 | Experimental                 |

## 🔹 Types of Transmission

- **Unicast**: One-to-one communication (single sender, single receiver).
- **Broadcast**: One-to-all communication (sent to all devices in a network).
- **Multicast**: One-to-many communication (sent to a group of subscribed devices).

## 🔹 Network Concepts

- **ARP (Address Resolution Protocol)**: Resolves IP to MAC addresses within a local network.
- **DHCP (Dynamic Host Configuration Protocol)**: Assigns IP addresses dynamically.
- **Subnetting**: Divides large networks into smaller ones to reduce congestion.
- **NAT (Network Address Translation)**: Maps private IPs to a public IP for internet access.

## 🔹 IPv4 vs IPv6

- **IPv4**: 32-bit address, limited address space, widely used.
- **IPv6**: 128-bit address, larger address pool, improved security & efficiency.

## 🔹 Reserved Address Blocks

| Type             | Range                         |
| ---------------- | ----------------------------- |
| **Private A**    | 10.0.0.0 - 10.255.255.255     |
| **Private B**    | 172.16.0.0 - 172.31.255.255   |
| **Private C**    | 192.168.0.0 - 192.168.255.255 |
| **Loopback**     | 127.0.0.0 - 127.255.255.255   |
| **Link-local**   | 169.254.0.0 - 169.254.255.255 |
| **Multicast**    | 224.0.0.0 - 239.255.255.255   |
| **Broadcast**    | 255.255.255.255               |
| **Experimental** | 240.0.0.0 - 255.255.255.254   |

---

**📝 Quick Tip:**
Remember that **private IPs** are used inside networks, while **public IPs** are unique across the internet. Loopback and link-local addresses are for special cases like self-communication and auto-configuration. 🚀
