# Topics Covered in this Lecture

- **IPv4 Address Classes** (Review)
- **Finding Network Parameters:**
  - Maximum number of hosts
  - Network address
  - Broadcast address
  - First and last usable address
- **Configuring IP addresses on Cisco devices**

---

## IPv4 Address Classes (Review)

### Key Points:
- **127.0.0.0** is reserved for loopback addresses.
- **0.0.0.0** is also reserved in Class A. Thus, Class A effectively ranges from **1.0.0.0 to 126.255.255.255**.
- Different sources may present slightly different ranges, but **remember Class A as 0-127**, knowing that 0 and 127 are reserved.

### Class Properties:
- **Class A**: 8 network bits, 24 host bits.
- **Class B**: 16 network bits, 16 host bits.
- **Class C**: 24 network bits, 8 host bits.

### Address Calculation:
- **Total addresses** in a network = `2^N`, where N is the number of host bits.
- **Usable addresses** = `2^N - 2` (subtract 2 for the network and broadcast addresses).

---

## Maximum Hosts Calculation

### Example: Class C Network (192.168.1.0/24)
- **Prefix length**: /24 (8 host bits).
- **Total addresses**: `2^8 = 256`.
- **Usable addresses**: `256 - 2 = 254`.

### Example: Class B Network (172.16.0.0/16)
- **Prefix length**: /16 (16 host bits).
- **Total addresses**: `2^16 = 65,536`.
- **Usable addresses**: `65,536 - 2 = 65,534`.

### Example: Class A Network (10.0.0.0/8)
- **Prefix length**: /8 (24 host bits).
- **Total addresses**: `2^24 = 16,777,216`.
- **Usable addresses**: `16,777,216 - 2 = 16,777,214`.

---

## Finding First and Last Usable Addresses

- **First usable address**: Network address + 1.
- **Last usable address**: Broadcast address - 1.

### Example: Class C (192.168.1.0/24)
- **Network address**: 192.168.1.0
- **First usable address**: 192.168.1.1
- **Broadcast address**: 192.168.1.255
- **Last usable address**: 192.168.1.254

### Example: Class B (172.16.0.0/16)
- **Network address**: 172.16.0.0
- **First usable address**: 172.16.0.1
- **Broadcast address**: 172.16.255.255
- **Last usable address**: 172.16.255.254

### Example: Class A (10.0.0.0/8)
- **Network address**: 10.0.0.0
- **First usable address**: 10.0.0.1
- **Broadcast address**: 10.255.255.255
- **Last usable address**: 10.255.255.254

---

## IP Address Configuration on Cisco Devices

### Example network:
- **Class A**: 10.0.0.0/8
- **Class B**: 172.16.0.0/16
- **Class C**: 192.168.0.0/24

### Configuration Steps:

1. **Entering Global Config Mode**: `conf t`
2. **Entering Interface Configuration Mode**:
   - `interface gigabitethernet0/0` (no space needed between interface name and number).
   - Shortcuts: `int g0/0` also works.
3. **Assigning IP Address**: 
   - `ip address [address] [subnet mask]`
   - Example: `ip address 10.255.255.254 255.0.0.0` for a /8 prefix.
4. **Enabling Interface**: `no shutdown`
5. **Verifying Configuration**: 
   - `show ip interface brief` (shortcut: `sh ip int br`) shows IPs, status, and protocol status.

---

### Key Concepts:
- **Status column**: Layer 1 status (physical connectivity).
- **Protocol column**: Layer 2 status (data link connectivity).
