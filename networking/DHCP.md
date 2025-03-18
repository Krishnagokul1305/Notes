# Dynamic Host Configuration Protocol (DHCP)

## What is DHCP?

DHCP (Dynamic Host Configuration Protocol) is a network management protocol used to automatically assign IP addresses and other network configuration settings to devices in a network. This eliminates the need for manual configuration and ensures efficient IP address allocation.

---

## How DHCP Works (Step-by-Step Process)

DHCP operates through a four-step process to assign network configurations to a client device when it connects to the network.

### **1. DHCP Discovery (Client Broadcasts Request)**

- When a device (client) joins the network, it does not have an IP address.
- The client sends a **DHCPDISCOVER** message as a broadcast to the entire network to find an available DHCP server.

### **2. DHCP Offer (Server Proposes an IP Address)**

- The DHCP server receives the DHCPDISCOVER message and responds with a **DHCPOFFER**.
- The offer includes:
  - A proposed **IP address**.
  - The **subnet mask** and **default gateway**.
  - The **lease time** (validity period of the IP address).
  - DNS server information.

### **3. DHCP Request (Client Accepts the Offer)**

- The client receives multiple offers but selects one DHCP server.
- It sends a **DHCPREQUEST** message to confirm the chosen IP address.
- Other DHCP servers withdraw their offers.

### **4. DHCP Acknowledgment (Server Confirms the Assignment)**

- The chosen DHCP server sends a **DHCPACK** (DHCP Acknowledgment) message.
- The client officially receives the assigned IP address and network settings.
- The IP address is **leased** for a specific duration before renewal is required.

![DHCP Flow](https://www.researchgate.net/publication/4109437/figure/fig4/AS:279599570276358@1443673140209/The-message-flow-of-DHCP-in-our-architecture.png)

---

## Types of DHCP IP Allocation

### **1. Dynamic Allocation**

- The DHCP server temporarily assigns an IP address.
- The lease must be renewed periodically.
- Common in office and home networks.

### **2. Automatic Allocation**

- The DHCP server remembers the device and assigns the same IP next time.
- The IP address remains the same unless manually changed.
- Used in internal company networks.

### **3. Static Allocation (Reservation)**

- The administrator manually assigns a specific IP address.
- The server links the IP address to the device’s **MAC address**.
- Used for **printers, servers, and security cameras**.

---

## Advantages of DHCP

✅ **Automates IP assignment** – No manual configuration needed.  
✅ **Prevents IP conflicts** – Ensures each device gets a unique IP.  
✅ **Centralized management** – Network admins can manage IP addresses efficiently.  
✅ **Supports mobility** – Devices can move between networks without needing reconfiguration.

---

## Conclusion

DHCP simplifies network management by automatically assigning IP addresses and configuration settings. It ensures efficient IP address usage and reduces manual workload for administrators.

For networks requiring **fixed IPs** for critical devices, **static allocation (reservation)** can be used within DHCP.

---
