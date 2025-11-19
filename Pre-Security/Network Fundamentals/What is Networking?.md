# What is Networking?

## Main Idea
- networks = connected things
- used in daily life and computing
- essential concept for cybersecurity

## What Is A Network
- things connected by common purpose
- applies to cities, power grids, postal systems
- computing uses same idea for devices

## Networks in Computing
- devices = phones, laptops, cameras, traffic lights, etc.
- networks can be 2 devices -> billions

---

## The Internet
- one giant network made of many smaller networks
- connects private networks together through public networks
- works like Alice connecting two groups who speak different languages

## How the Internet Started
- ARPANET created in late 1960s
- funded by US Defence Department
- 1989: Tim Berners-Lee created the World Wide Web
- WWW allowed storing and sharing information

## Types of Networks
- private networks: smaller internal networks
- public networks: connect private networks together
- the internet = public networks linking many private networks

## Device Identification
- devices use labels to identify themselves on networks
- topic covered in next task

---

## IP Addresses
- IP = Internet Protocol address
- identifies a device on a network for a period of time
- can be reused by another device later
- an IP address = four octets
- only one device can use the same IP within the same network at the same time

## Public vs Private IPs
- public IP: identifies a device on the Internet
- private IP: identifies a device inside a private network
- devices talk to each other using private IPs
- data sent to the Internet is identified by the same public IP from the ISP
- public IPs are limited and assigned by an ISP

## IPv4 and IPv6
- IPv4: 2^32 addresses (~4.29 billion)
- shortage due to number of connected devices
- IPv6: 2^128 addresses (340 trillion+)
- more efficient and solves IPv4 exhaustion

## MAC Addresses
- assigned to physical network interface at factory
- 12-character hexadecimal number split into pairs with colons
- first six characters: manufacturer
- last six: unique device identifier

## MAC Spoofing
- MAC addresses can be faked ("spoofed")
- spoofing can break weak security relying only on MAC addresses trust
- example: firewall trusts admin MAC, attacker spoofs it and gains access

## MAC Control in Public Wi-Fi
- cafes and hotels often use MAC-based access control
- can restrict or charge per device
- spoofing can bypass restrictions
