# IP Address Ranges and Their Types

This document provides a comprehensive list of IP address ranges and their classifications. Each type of IP address serves a different purpose in networking, from private communication to global internet routing.

## IP Address Classification Table

| **Type**                         | **IPv4 Range**                                                                            | **IPv6 Range**                        | **Description**                                                      |
| -------------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------- | -------------------------------------------------------------------- |
| **Unicast (Public)**             | 1.0.0.0 - 223.255.255.255                                                                 | Everything except reserved ranges     | Standard addresses used for communication on the internet.           |
| **Unicast (Private)**            | 10.0.0.0 - 10.255.255.255<br>172.16.0.0 - 172.31.255.255<br>192.168.0.0 - 192.168.255.255 | FC00::/7 (ULA - Unique Local Address) | Used within private networks (not routable on the internet).         |
| **Loopback**                     | 127.0.0.0 - 127.255.255.255                                                               | ::1                                   | Used for internal communication within a device (localhost).         |
| **Link-Local**                   | 169.254.0.0 - 169.254.255.255                                                             | FE80::/10                             | Auto-assigned when no DHCP is available; used within local networks. |
| **Multicast**                    | 224.0.0.0 - 239.255.255.255                                                               | FF00::/8                              | Used for one-to-many communication (e.g., streaming, routing).       |
| **Broadcast**                    | 255.255.255.255                                                                           | Not used (IPv6 uses multicast)        | Sends data to all devices in a network.                              |
| **Reserved**                     | 240.0.0.0 - 255.255.255.254                                                               | Reserved by IANA                      | Reserved for future use or special purposes.                         |
| **Documentation / Testing**      | 192.0.2.0 - 192.0.2.255<br>198.51.100.0 - 198.51.100.255<br>203.0.113.0 - 203.0.113.255   | 2001:DB8::/32                         | Used for examples and documentation.                                 |
| **APIPA (Automatic Private IP)** | 169.254.0.0 - 169.254.255.255                                                             | FE80::/10                             | Automatically assigned when DHCP is unavailable.                     |
| **Anycast**                      | Not specific to an IP range                                                               | Any unicast address can be used       | A single IP assigned to multiple devices for routing efficiency.     |

## Notes

- **Private IP addresses** are used within local networks and are not accessible from the public internet.
- **Loopback addresses** allow a device to communicate with itself for testing and development purposes.
- **Link-local addresses** are self-assigned and facilitate local network communication without a DHCP server.
- **Multicast addresses** are used for sending data to multiple devices simultaneously.
- **Broadcast addresses** allow messages to be sent to all devices on a network.
- **Reserved addresses** are held for future use or special purposes by IANA.

![ip-ranges](https://labs.ripe.net/media/images/Pre-1993-IP-addresses.width-640.png)
