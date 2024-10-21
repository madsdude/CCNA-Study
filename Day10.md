
## Video Overview

In this video, we’ll explore the **Internet Protocol version 4 (IPv4) header**.

- **Purpose**: The IPv4 header is used at **Layer 3** to route data between devices, even across the world through the Internet.
- Originally planned as a broad routing introduction, the topic has been divided into multiple parts for better depth.

---

## Topics Covered

1. **IPv4 Packet Structure**: Focus on the **IPv4 header**, which encapsulates a TCP or UDP segment.
2. **IPv4 Header Fields**: A detailed examination of each field in the header.

---

## OSI Model Review - PDUs

- Upper layers prepare data, encapsulated in the **Layer 4 header** (TCP/UDP), forming a **segment**.
- **Layer 3 header** (IPv4) is added, forming a **packet**.
- **Layer 2 header and trailer** are added, forming a **frame**.
- **Protocol Data Units (PDUs)**:
  - Layer 3 PDU: Packet
  - Layer 2 PDU: Frame

For this lesson, we focus on the **Layer 3 IPv4 header**.

---

## IPv4 Header Overview

The IPv4 header contains several fields that help in routing packets across networks. We’ll go through each field to understand its purpose.

---

### IPv4 Header - Version Field

- **Length**: 4 bits.
- **Purpose**: Identifies the **IP version** used.
  - Value of **4** indicates **IPv4**.
  - Value of **6** indicates **IPv6**.

---

### IPv4 Header - IHL (Internet Header Length) Field

- **Length**: 4 bits.
- **Purpose**: Specifies the **length of the header** in 4-byte increments.
  - Minimum value: 5 (20 bytes).
  - Maximum value: 15 (60 bytes).
  
---

### IPv4 Header - DSCP (Differentiated Services Code Point) Field

- **Length**: 6 bits.
- **Purpose**: Used for **QoS** (Quality of Service) to prioritize delay-sensitive data (e.g., voice and video).

---

### IPv4 Header - ECN (Explicit Congestion Notification) Field

- **Length**: 2 bits.
- **Purpose**: Notifies end devices about **network congestion** without dropping packets.

---

### IPv4 Header - Total Length Field

- **Length**: 16 bits.
- **Purpose**: Indicates the **total length** of the packet, including the header and encapsulated data.
  - Minimum: 20 bytes (header only).
  - Maximum: 65,535 bytes.

---

### IPv4 Header - Identification Field

- **Length**: 16 bits.
- **Purpose**: Used to identify fragments of the same packet for reassembly.

---

### IPv4 Header - Flags Field

- **Length**: 3 bits.
- **Purpose**: Controls and identifies fragments.
  - **Bit 0**: Reserved (always 0).
  - **Bit 1**: **DF (Don’t Fragment)** bit.
  - **Bit 2**: **MF (More Fragments)** bit.

---

### IPv4 Header - Fragment Offset Field

- **Length**: 13 bits.
- **Purpose**: Indicates the position of the fragment within the original packet to assist in reassembly.

---

### IPv4 Header - Time To Live (TTL) Field

- **Length**: 8 bits.
- **Purpose**: Prevents packets from looping infinitely by decrementing the TTL at each router. If TTL reaches 0, the packet is dropped.

---

### IPv4 Header - Protocol Field

- **Length**: 8 bits.
- **Purpose**: Indicates the **Layer 4 protocol** (e.g., TCP = 6, UDP = 17, ICMP = 1).

---

### IPv4 Header - Header Checksum Field

- **Length**: 16 bits.
- **Purpose**: Used to detect errors in the IPv4 header.

---

### IPv4 Header - Source and Destination IP Address Fields

- **Length**: 32 bits each.
- **Purpose**:
  - **Source IP**: IPv4 address of the sender.
  - **Destination IP**: IPv4 address of the recipient.

---

### IPv4 Header - Options Field

- **Length**: Variable (0–320 bits).
- **Purpose**: Rarely used but allows for additional options to be included in the IPv4 header.

---

## Wireshark Packet Capture

- Wireshark is a tool used to analyze network traffic. In this course, we’ll examine IPv4 packets using Wireshark.
- Example of a **ping** packet and its **IPv4 header** fields:
  - Version: 4
  - Header length: 20 bytes (no options)
  - TTL: 255
  - Protocol: ICMP (1)

---

## Things We Covered

1. **IPv4 header structure** and the purpose of each field.
2. An introduction to **Wireshark** for packet analysis.

---

## Quiz Time

- Use the Anki flashcards linked in the description to help remember the details covered in this video.
- **First quiz question**: What is the fixed binary value of the first field of an IPv4 header?
