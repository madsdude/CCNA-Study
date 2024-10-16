## Introduction to Routing

This is the 7th lecture in the series. In the past couple videos, we talked about Ethernet LAN switching, for example within this small network of PCs attached to a switch. In this video, however, we’ll start to expand our horizon and take a look at how traffic is forwarded not WITHIN a LAN, but between different LANs. Basically, we are going up the OSI model from Layer 2 (the data link layer) to Layer 3 (the network layer).

### OSI Model - Network Layer Review

- **Layer 3 (Network Layer)**: 
    - Provides connectivity between end hosts on different networks outside of the local area network (LAN).
    - Uses **IP addresses** for logical addressing.
    - Involves **path selection** to determine the best route for data to reach its destination in more complex networks like the Internet.
    - **Routers** operate at Layer 3, facilitating communication between different networks.

### Logical Layer 3 Addresses: IP Addresses

You may recognize this network from the previous videos on Ethernet LAN switching. These PCs are all connected by switches, so they are part of the same network. **Layer 2 devices** (switches) do not separate different networks; they connect and expand networks. 

For example, all PCs in the same network may have IP addresses in the **192.168.1.0/24** network:
- PC1: 192.168.1.1
- PC2: 192.168.1.2
- PC3: 192.168.1.3
- PC4: 192.168.1.4

However, when we introduce a **router** between switches, the network becomes split into two:
- Network 1: **192.168.1.0/24**
    - PC1 and PC2 belong here.
- Network 2: **192.168.2.0/24**
    - PC3 and PC4 belong here.

The router will also have IP addresses for each network it connects to:
- R1’s **G0/0** interface: 192.168.1.254
- R1’s **G0/1** interface: 192.168.2.254

Broadcasts are limited to their local network and won’t cross the router.

### IPv4 Addresses

An IPv4 address consists of **32 bits** (or **4 bytes**). For example, the address **192.168.1.254** is represented in binary as follows:
- 192 = 11000000
- 168 = 10101000
- 1 = 00000001
- 254 = 11111110

This is known as **dotted decimal notation**, which is more human-readable compared to binary.

### Binary and Decimal Review

- **Decimal (Base 10)**: In decimal, each digit increases by a factor of 10.
- **Hexadecimal (Base 16)**: Each digit increases by a factor of 16.
- **Binary (Base 2)**: Each digit increases by a factor of 2.

For example, the number **192** in binary is **11000000**. Understanding binary is crucial for working with IPv4 addresses.

### IPv4 Address Classes

IPv4 addresses are categorized into different classes based on their first octet:
- **Class A**: Range 0-127, prefix length /8.
- **Class B**: Range 128-191, prefix length /16.
- **Class C**: Range 192-223, prefix length /24.
- **Class D**: Reserved for multicast (224-239).
- **Class E**: Reserved for experimental use (240-255).

### Special Address Ranges

- **Loopback Addresses (127.x.x.x)**: These are reserved for testing the network stack of a local device. For example, **127.0.0.1** is used to send pings to the local device.
  
### Netmasks and Prefix Lengths

- **Netmask**: Specifies the network and host portions of an IP address. A **netmask** for a Class C network would be **255.255.255.0**.
- The prefix length can also be written in a simpler way as **/24**, which indicates that the first 24 bits of the address are for the network, and the remaining 8 bits are for hosts.

### Network and Broadcast Addresses

- **Network Address**: The address that represents the entire network (e.g., **192.168.1.0/24**).
- **Broadcast Address**: The address used to send data to all hosts on the network (e.g., **192.168.1.255**).

The network address is the first address in the range, while the broadcast address is the last.

### Recap

- IPv4 addresses are divided into a network portion and a host portion.
- We covered binary and dotted decimal representations of IPv4 addresses.
- You learned about different address classes and special ranges like the loopback address.
- We also discussed netmasks and how they relate to prefix lengths.

![Skærmbillede 2024-10-16 144002](https://github.com/user-attachments/assets/1d84269f-2c31-42ba-97af-bbb07e2a7291)

![Skærmbillede 2024-10-16 144018](https://github.com/user-attachments/assets/928d0024-c471-4507-84e6-4840b540b13c)

![Skærmbillede 2024-10-16 144112](https://github.com/user-attachments/assets/8b24ae0f-0b78-40bc-b2bb-6eb5d09e5990)


