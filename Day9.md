
## Overview of the Video

- **Focus**: Switching from IP addresses to **switch interfaces**.
- **Topics covered**:
  - Configuring Layer 1 characteristics of switch interfaces such as **speed** and **duplex**.
  - **Autonegotiation** for speed and duplex settings.
  - **Interface status** on switches.
  - **Interface counters and errors** on Cisco devices.

---

## Switch vs Router Interfaces

### Key Points:
- Router interfaces are **administratively disabled** by default (`shutdown` command applied).
- Switch interfaces **do not** have the `shutdown` command applied by default.
  - **Switch interfaces** are usually **up/up** if connected to another device, even without configuration.
  - Unconnected interfaces show a **down/down** status.

---

## Network Topology Used in the Video

- **Single LAN**: `192.168.1.0/24`
- Devices:
  - **Router (R1)**
  - **Switches (SW1, SW2)**
  - **PCs (PC1, PC2, PC3, PC4)**

---

## Commands Covered

### `show ip interface brief`
- Displays Layer 1 and Layer 2 status for interfaces:
  - **up/up**: Connected and operational.
  - **down/down**: Not connected.
  - **administratively down/down**: Interface has the `shutdown` command applied.

### `show interfaces status`
- Displays detailed information on switch interfaces:
  - **Status**:
    - `connected`: Interface is active.
    - `notconnect`: Interface is not connected.
  - **VLAN**: Default VLAN is 1.
  - **Duplex**: Indicates whether the interface is using **full** or **half** duplex.
  - **Speed**: Displays the negotiated speed (e.g., `a-100` means 100 Mbps auto-negotiated).
  - **Type**: Physical interface type (e.g., `10/100BASE-TX`).

---

## Configuring Speed and Duplex

- Enter **interface configuration mode**:
  - Example: `interface fastethernet 0/1`
- **Set speed**:
  - Example: `speed 100` (sets the speed to 100 Mbps).
- **Set duplex**:
  - Example: `duplex full` (sets the interface to full duplex).
- **Description**: Set a description for clarity:
  - Example: `description Connected to R1`

### Verifying Configuration:
- Use `show interfaces status` to confirm:
  - Speed and duplex will display without the `a-` prefix when manually configured.

---

## Disabling Unused Interfaces

- To enhance security, unused interfaces should be **disabled**:
  - Use the **range command** to configure multiple interfaces at once:
    - Example: `interface range fastethernet 0/5 to 12`
  - Disable the interfaces: `shutdown`
  - Use `no shutdown` to re-enable specific interfaces if needed.

---

## Full and Half Duplex

### Key Concepts:
- **Half duplex**: 
  - Device cannot send and receive data at the same time.
  - Used in **hub** networks.
  - **Collision domain**: All devices share the same transmission medium.
  - **CSMA/CD**: Used to manage collisions in half-duplex networks.
- **Full duplex**:
  - Device can send and receive data simultaneously.
  - Used in modern **switch** networks.

---

## Speed/Duplex Autonegotiation

- **Autonegotiation** allows devices to automatically select the appropriate speed and duplex settings.
- Example:
  - A switch port and device negotiate to the **maximum supported speed** (e.g., 10/100/1000 Mbps) and **full duplex** if supported.
- If autonegotiation fails:
  - Switch uses the **lowest supported speed** and defaults to **half duplex** for speeds below 1000 Mbps.

---

## Interface Errors and Counters

### Key Counters:
- **Runts**: Frames smaller than 64 bytes.
- **Giants**: Frames larger than 1518 bytes.
- **CRC errors**: Frames that failed the cyclic redundancy check (FCS check).
- **Frame errors**: Frames with illegal formats.
- **Input errors**: Sum of all input errors.
- **Output errors**: Frames that failed to send.

---

## Summary of Topics Covered

- **Interface speed and duplex** settings, including the difference between **full** and **half duplex**.
- **Autonegotiation** for speed and duplex.
- **Interface status** using the `show interface status` command.
- **Interface errors** such as runts, giants, and CRC errors.

---

## Quiz Time

- Flashcards and practice exercises are available for further study (see link in description).
