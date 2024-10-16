# Ethernet Frame

- **Components**: An Ethernet frame is composed of several important fields that help ensure the correct delivery of data between devices on a local area network (LAN). These include:
  - **Preamble**: A 7-byte sequence that helps synchronize communication between devices by indicating the start of a frame.
  - **Start Frame Delimiter (SFD)**: A single byte that signals the actual beginning of the frame.
  - **Destination MAC**: The MAC address of the intended recipient of the frame.
  - **Source MAC**: The MAC address of the sender of the frame.
  - **Type**: Specifies the type of protocol encapsulated in the frame (for example, IPv4 is 0x0800).

- **Size**: Ethernet frames have a minimum size of 64 bytes. This includes both the headers and the payload. If the actual payload is smaller than 46 bytes (since the header is 18 bytes), additional padding bytes are inserted to meet the minimum frame size. The padding consists of zeros and ensures reliable data transmission.

# Network Example

- **Small Network with Three PCs**: In a basic network, devices communicate using both IP addresses (Layer 3) and MAC addresses (Layer 2). IP addresses serve as logical identifiers, while MAC addresses are unique hardware addresses.

- **MAC Addresses**: These are 48-bit (6-byte) addresses, typically written in hexadecimal format. The first 3 bytes of the MAC address are known as the **OUI (Organizationally Unique Identifier)**, which identifies the manufacturer of the device. The last 3 bytes are unique to each device.

- **IP Addresses**: Each device in the network also has a unique IP address that identifies it logically on the network. For example:
  - PC1: 192.168.1.1
  - PC2: 192.168.1.2
  - PC3: 192.168.1.3

# ARP (Address Resolution Protocol)

- **Purpose**: ARP is used to map an IP address (Layer 3, logical address) to a MAC address (Layer 2, hardware address). This is necessary because devices use IP addresses for logical communication but need the MAC address to send data over the local network.

- **ARP Request**: When a device knows the destination IP but not the MAC address, it sends a broadcast frame containing an ARP request. The broadcast frame is sent to all devices on the local network, asking, "Who has this IP address?"

- **ARP Reply**: The device with the matching IP responds with an ARP reply, which is a unicast frame. The ARP reply contains the MAC address of the device with the requested IP address, allowing the original sender to map the IP to the correct MAC address.

- **Process**:
  1. Device A sends an ARP request to all devices on the network.
  2. Device B, with the matching IP, replies with its MAC address.
  3. Device A stores this information in its ARP table for future communication.

# MAC Address Table on Switches

- **Dynamic Entries**: A switch learns MAC addresses dynamically by examining the source MAC address of incoming frames. Each learned MAC address is associated with a specific port, allowing the switch to forward traffic to the correct device.

- **Aging**: Dynamic entries in the MAC address table are temporary. If no traffic is seen from a MAC address for a certain period (typically 5 minutes), the entry is removed. This is called aging, and it helps the switch conserve memory and prevent the table from becoming outdated.

- **Manual Clearing**: Network administrators can manually clear dynamic entries from the MAC address table using specific commands. This is useful for troubleshooting or resetting the table.

# Ping Utility

- **Purpose**: Ping is a basic network utility used to test whether one device can communicate with another over a network. It sends small data packets and measures the round-trip time to ensure the two devices are reachable.

- **Messages**:
  - **ICMP Echo Request**: This message is sent from the source device to the destination, asking if the destination is reachable.
  - **ICMP Echo Reply**: The destination responds with this message if it successfully receives the echo request.

  Ping is widely used for basic network troubleshooting and verifying connectivity between devices.

# Wireshark Packet Capture

- **Purpose**: Wireshark is a network analysis tool that allows you to capture and inspect packets traversing a network. It can show details of different protocols, including ARP and ICMP.

- **ARP and ICMP Inspection**: When capturing traffic related to ARP and ICMP, Wireshark can display the details of the messages, such as MAC addresses and IP addresses used in the communication. This is helpful for analyzing how devices discover each other and test connectivity.

# Clearing Dynamic Entries from the MAC Address Table

- **Commands**: There are different commands available for managing the MAC address table:
  - **Clear all dynamic entries**: You can remove all dynamically learned entries from the MAC address table, effectively resetting the table.
  - **Clear specific entries**: This allows you to target and remove specific MAC addresses from the table.
  - **Clear entries by interface**: You can also clear all dynamic entries associated with a particular switch port or interface.
