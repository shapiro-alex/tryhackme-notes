# Packets and Frames

## Main Idea
- **packet** = Layer 3 data (IP info)
- **frame** = Layer 2
- frames **encapsulate** packets

## Packet (Layer 3 - Network)
- contains IP header + payload
- used when discussing anything with **IP addresses**
- broken into small pieces for efficient transfer
- reconstruted on the destination device

## Frame (Layer 2 - Data Link)
- wraps the packet
- adds **MAC addresses** (source + destination)
- like an envelope that carries the letter (packet)

## Why This Matters
- smaller chunks prevent bottlenecks
- standardised structure keeps devices communicating correctly

## Common Packet Headers
- **TTL** - Time To Live (prevents stuck packets)
- **Checksum** - integrity check
- **Source Address** - sender's IP
- **Destination Address** - target IP

---

# TCP (Transmission Control Protocol)

## Main Idea
- connection-based protocol
- guarantees delivery and correct order
- uses **encapsulation** and **decapsulation**
- follows the 4-layer TCP/IP model:
  - Application
  - Transport
  - Internet
  - Network Interface

## Why TCP Matters
- must form a connection before sending data
- ensures accuracy, reliability, and proper sequency

## Pros
- guaranteed integrity
- prevents flooding/keeps data in order
- reliable communication

## Cons
- slower than UDP
- requires stable connection
- more overhead

## TCP Headers
- **Source Port** — sender’s port (random 0–65535)  
- **Destination Port** — service port on receiver (ex: 80)  
- **Source IP** — sender’s IP  
- **Destination IP** — receiver’s IP  
- **Sequence Number** — ordering of data  
- **Acknowledgement Number** — confirms next expected number  
- **Checksum** — integrity check  
- **Data** — actual bytes being sent  
- **Flag** — controls handshake/behavior  

## Three-Way Handshake
1. **SYN** — client requests connection  
2. **SYN/ACK** — server acknowledges + syncs  
3. **ACK** — client confirms; connection established

## Common Flags
- **SYN** — start connection  
- **ACK** — acknowledge  
- **DATA** — actual information sent  
- **FIN** — graceful close  
- **RST** — force close (error/problem)

## Example (Sequence Numbers)
- client sends SYN with ISN (Initial Sequence Number)  
- server replies with its own ISN + ACK  
- client ACKs server’s ISN  
- data increments sequence numbers by +1 each time  

## Closing a TCP Connection
- device sends **FIN**  
- other device **ACKs**  
- second device sends **FIN**  
- first device **ACKs**  
- connection ends cleanly

---

# UDP (User Datagram Protocol)

- stateless, no connection setup
- no Three-way handshake
- no sync, no guarantees

## When Used
- apps can tolerate lost data
- streaming, voice chat, ARP, DHCP

## Pros
- must faster than TCP
- flexible for developers
- no connection reserved

## Cons
- no guarantee data is received
- no integrity checks
- unstable networks = bad experience

## UDP Headers
- **TTL (Time To Live)** — prevents stuck packets  
- **Source Address** — sender IP  
- **Destination Address** — receiver IP  
- **Source Port** — random sender port  
- **Destination Port** — service port (ex: 80)  
- **Data** — actual bytes

## Key Concept
- sends data with no ACKs  
- no ordering, no recovery

---

# Ports

- ports = numbered endpoints for sending/receiving data
- range: **0-65535**
- like harbour ports: only certain "ships" (protocols) can dock

## Why Ports Matter
- enforce which application handles which traffic
- prevent chaos by standardising rules
- ex: all web browsers send HTTP over **port 80**

## Common Ports (0-1024)
- **21 FTP** - file transfers
- **22 SSH** - secure remote login
- **80 HTTP** - web traffic
- **443 HTTPS** - encrypted web
- **445 SMB** - file/printer sharing
- **3389 RDP** - remote desktop

## Notes
- standards = defaults, but apps can use other ports (ex: :8080)
- clients must specify the port if nonstandard
