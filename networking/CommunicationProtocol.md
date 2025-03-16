# Networking Protocols

## Introduction

A **protocol** in networking is a set of rules that define how data is transmitted and received over a network. These rules ensure smooth communication between devices, regardless of their manufacturers or underlying hardware.

## Why Are Protocols Important?

Protocols are essential because they:

- Standardize communication between devices.
- Ensure data is transmitted correctly and securely.
- Allow different devices and applications to work together seamlessly.

## Common Networking Protocols

Here are some widely used networking protocols:

1. **HTTP (Hypertext Transfer Protocol)** - Used for browsing websites.
2. **HTTPS (Secure HTTP)** - A secure version of HTTP that encrypts data.
3. **TCP/IP (Transmission Control Protocol/Internet Protocol)** - The foundation of internet communication.
4. **FTP (File Transfer Protocol)** - Used for transferring files between computers.
5. **SMTP (Simple Mail Transfer Protocol)** - Helps in sending emails.
6. **DNS (Domain Name System)** - Translates domain names into IP addresses.

## TCP/IP Model

The **TCP/IP model** is a framework that defines how data is sent and received over the internet. It consists of **four layers**, each with a specific role in communication.

### **TCP/IP Model Layers:**

1️⃣ **Application Layer (User Interaction)**

- This layer handles communication between applications (e.g., web browsers, email clients).
- It uses protocols like **HTTP, FTP, SMTP, and DNS** to format and send data.
- **Example:** When you type a website address in a browser, HTTP sends a request to the web server.

2️⃣ **Transport Layer (Reliable Data Delivery) – 🔹TCP Works Here**

- **TCP (Transmission Control Protocol) operates in this layer.**
- **TCP is responsible for:**
  - Establishing a connection (using a three-way handshake: SYN → SYN-ACK → ACK).
  - Splitting data into packets (ensuring proper order and completeness).
  - Checking for errors and retransmitting lost packets if needed.
- **UDP (User Datagram Protocol)** also works here but does not guarantee reliability like TCP.

3️⃣ **Internet Layer (Addressing & Routing) – 🔹IP Works Here**

- **IP (Internet Protocol) operates in this layer.**
- **IP is responsible for:**
  - Assigning a **unique IP address** to sender and receiver.
  - Routing packets across networks to their destination.
  - **Does NOT ensure reliable delivery** (this is handled by TCP at the transport layer).
- Other protocols like **ICMP (error messages) and ARP (address resolution)** also work here.

4️⃣ **Network Access Layer (Physical Data Transfer)**

- Converts **packets into signals** (electrical, optical, or wireless) for transmission over **Ethernet, Wi-Fi, or fiber cables**.
- Ensures that data physically reaches the next device in the network.

### **TCP/IP Model Diagram:**

![TCP/IP Model](https://media.geeksforgeeks.org/wp-content/uploads/20230904204434/IMG_20230904_204347.jpg)

### **How TCP/IP Works:**

1. You type a website address (**Application Layer** - HTTP).
2. Data is split into packets and ordered correctly (**Transport Layer** - TCP).
3. The packets are assigned addresses and routed across the internet (**Internet Layer** - IP).
4. Data is physically transmitted via cables or Wi-Fi (**Network Access Layer** - Ethernet/Wi-Fi)

### **TCP/IP and OSI Model Diagram:**

![TCP/IP and OSI Model](https://media.geeksforgeeks.org/wp-content/uploads/20230417045622/OSI-vs-TCP-vs-Hybrid-2.webp)

# OSI Model (Open Systems Interconnection Model)

![ OSI Model](https://blog.smartbuildingsacademy.com/hubfs/What%20is%20the%20OSI%20Model.png)

### 1️⃣ Application Layer (User Interaction)

- Directly interacts with user applications like web browsers and email clients.
- Uses protocols such as **HTTP, FTP, SMTP, and DNS**.
- **Example:** When you enter a website URL, HTTP requests the webpage from a server.

### 2️⃣ Presentation Layer (Data Formatting & Encryption)

- Converts data into a format that applications can understand.
- Handles encryption, compression, and encoding (e.g., **SSL/TLS for HTTPS**).
- **Example:** When you access a secure website, TLS encrypts your data.

### 3️⃣ Session Layer (Managing Connections)

- Establishes, maintains, and terminates communication sessions.
- **Example:** When you log into a website, your session remains active until you log out.

### 4️⃣ Transport Layer (Reliable Data Delivery)

- Ensures end-to-end communication between devices.
- Uses **TCP (reliable, ordered transmission)** and **UDP (faster but unreliable)**.
- **Example:** TCP ensures all packets of a file download arrive correctly.

### 5️⃣ Network Layer (Routing & IP Addressing)

- Finds the **best path** for data to reach its destination.
- Uses **IP (Internet Protocol) for addressing** and **routers for packet forwarding**.
- **Example:** When you visit a website, your request is routed through multiple networks.

### 6️⃣ Data Link Layer (Error Detection & MAC Addressing)

- Ensures reliable transmission between two devices on the same network.
- Uses **MAC (Media Access Control) addresses** for device identification.
- **Example:** Ethernet and Wi-Fi protocols work at this layer.

### 7️⃣ Physical Layer (Hardware & Transmission)

- Converts data into electrical, optical, or wireless signals for transmission.
- Includes cables, switches, and network interface cards (NICs).
- **Example:** A Wi-Fi router transmitting data signals.

## OSI Model vs. TCP/IP Model

| Feature              | OSI Model (7 Layers)                | TCP/IP Model (4 Layers)              |
| -------------------- | ----------------------------------- | ------------------------------------ |
| **Usage**            | Theoretical model for networking    | Practical model used in the internet |
| **Number of Layers** | 7                                   | 4                                    |
| **Main Function**    | Standardizing network communication | Internet communication               |
| **Reliability**      | Provides strict modularity          | More flexible and widely used        |
