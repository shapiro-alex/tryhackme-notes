# OSI Model (Open Systems Interconnection)

## Main Idea
- standard model for how devices communicate
- ensures all systems follow the same structure

## Purpose
- divides networking into 7 layers
- each layer has a specific role
- helps different devices work together

## Layers (7 -> 1)
7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data link
1. Physical

## Key Concept
- encapsulation = each layer adds its own info as data moves down the stack

---

## Layer 1: Physical
- physical hardware layer
- sends data as electrical/light signals (binary, 1s and 0s)
- lowest OSI layer
- examples: ethernet cables, physical connectors

---

## Layer 2: Data link
- adds **MAC address** (physical address)
- NIC (network interface card) has a unique burnt-in MAC
- MAC = used to locate the exact destination device
- MAC can be spoofed
- prepares data into a format suitable for transmission

---

## Layer 3: Network
- handles **routing** + **reassembly** of data
- decides the **best path** using routin protocols
  - OSPF = Open Shortest Path First
  - RIP = Routing Information Protocol
- routing choices based on:
  - shortest path (fewest hops)
  - most reliable path (least packet loss)
  - fastest medium (fiber > copper)
- uses **IP addresses** for delivery
- routers work at **Layer 3**

---

## Layer 4: Transport

## Purpose
- handles **data delivery**
- uses two protocols: **TCP** (Transmission Control Protocol) and **UDP** (User Datagram Protocol)

## TCP (Transmission Control Protocol)
- reliable, accurate, ordered
- constant connection between devices
- error-checking + reassembly
- used for: web browsing, file transfer, email

**Pros**
- guaranteed delivery
- keeps devices in sync

**Cons**
- slower
- needs stable connection

## UDP (User Datagram Protocol)
- fast, no guarantee, no error-checking
- sends data without checking if it arrived
- used for: streaming, ARP, DHCP, discovery

**Pros**
- very fast
- low overhead

**Cons**
- packets may be lost
- bad for unstable connections

  

---

## Layer 5: Session
- creates and maintains the **session** (connection) between devices
- session stays active while communication is happening
- closes the session if unused or lost
- can set **checkpoints** so only new data must be resent if lost
- each session is **unique** - data stays within its own session

---

## Layer 6: Presentation
- handles **formatting** and **standardization** of data
- acts as a **translator** between apps and the lower layers
- ensures different software (ex: different email clients) can display the same data
- handles **encryption/decryption** (ex: HTTPS)

---

## Layer 7: Application
- the layer user interacts with
- defines how applications **send and receive data**
- uses protocols that support user-facing tasks
- examples: web browsers, email clients, file transfer apps (FileZilla)

### Common Protocols
- **DNS** - Domain Name System (translates domain names to IP addresses)
- **HTTP/HTTPS** - web browsing
- **SMTP/IMAP/POP3** - email

---
