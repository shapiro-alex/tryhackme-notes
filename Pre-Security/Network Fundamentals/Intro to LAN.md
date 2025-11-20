# Intro to LAN

## Main Idea
- LAN = Local Area Network
- covers a small physical area (home, office, school)
- different LAN topologies exist with different pros/cons

## Star Topology
- devices connect to a central switch or hub
- most common modern topology
- scalable and reliable
- more expensive (extra cabling + hardware)
- easy to add devices
- failure of central device = network down
- harder maintenance as it scales

## Bus Topology
- uses a single backbone cable
- devices branch off like "leaves"
- cheap and easy to set up
- prone to bottlenecks (all traffic on one cable)
- hard to troubleshoot
- single point of failure: if backbone breaks, network dies

## Ring Topology
- devices connected in a loop
- minimal cabling, no central hardware needed
- data travels in one direction around the ring
- easy to troubleshoot
- not efficient (data may pass many devices)
- less bottlenecking than us
- one broken device or cable breaks the whole ring

## Switches
- connect multiple devices on a LAN
- ports: 4, 8, 16, 24, 32, 64
- smarter than hubs/repeaters
- keep track of which device is on which port
- send packets only to intended device -> reduces traffic
- switches and routers can be linked for redundancy

## Routers
- connect different networks together
- move data between networks using routing
- create paths for data to travel across networks
- essential for connecting LAN to other LANs or to the internet

---

## Subnetting

### Main Idea
- subnetting = splitting a big network into smaller networks
- like dividing a cake into slices
- used to organize departments (accounting, HR, finance, etc.)

### What Subnetting Does
- divides devices into smaller groups
- helps networks know where information should go
- controlled using a **subnet mask** (32 bits total, 4 octets, 0-255)

### Subnets Use IP to Identify
- **Network Address** - start of the network (ex: `192.168.1.0`)
- **Host Address** - specific device (ex: `192.168.1.100`)
- **Default Gateway** - device that sends traffic to other networks (usually `.1` or `.254`)

### Small vs Large Networks
- home networks usually = 1 subnet (less than 254 devices)
- businesses need multiple (PCs, printers, cameras, sensors)

### Benefits
- efficiency
- security
- more control

### Example Use Case
- cafe uses two subnets:
  - employee devices + registers
  - public guest Wi-Fi
- subnetting keeps them separated but still connected to the internet

---

## ARP (Address Resolution Protocol)

### Main Idea
- ARP links an IP address to a MAC address
- lets devices identify each other on a LAN
- every device keeps a small ARP cache (a ledger of IP -> MAC pairs)

### How ARP Works
- device needs to talk to another -> must know its MAC
- ARP sends two message types:
  - **ARP Request** - "who has this IP?"
  - **ARP Reply** - device answers with its MAc if the IP is theirs

### ARP Process
- device broadcasts an ARP request to the entire network
- only the device with that IP replies with its MAC address
- requester stores the result in its ARP cache
- next time, it won't need to ask again

### Purpose
- maps IP (logical identifier) -> MAC (physical identifier)
- enables communication inside a LAN

---
## DHCP (Dynamic Host Configuration Protocol)

### Main Idea
- assigns IP addresses automatically
- avoids manual setup for every device
- used on almost all modern networks

### Why DHCP Matters
- gives devices IPs, subnet mask, gateway, DNS, etc.
- makes network setup fast and consistent

### DHCP Processes (DORA)
- **Discover:** - device broadcasts "I need an IP"
- **Offer** - DHCP server offers an IP (example: `192.168.1.10`)
- **Request** - device accepts that offered IP
- **ACK** - server confirms the lease; device can use the IP

### Notes
- assigned IP usually has a **lease time** (e.g., 24 hours)
- if no DHCP server exists, device must be configured manually
