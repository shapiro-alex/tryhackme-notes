# Extending Your Network

- allows internal services (ex: a webserver) to be reachable from the Internet
- without it, apps are only available inside the same local network (intranet)

## How It Works
- router maps **public IP + port** -> **internal IP + port**
- ex: 82.62.51.70:80 -> 192.168.1.10:80
- lets outside devices reach an internal machine

## Port Forwarding vs Firewall
- **port forwarding** = opens a port and directs traffic to a device
- **firewall** = decides whether traffic is allowed through the port

## Where It's Configured
- set on the **router**

---

# Firewalls

- control what traffic is allowed **in** or **out** of a network
- act like border security
- destinations based on: source, destination, port, protocol
- usually operate at **OSI layers 3 & 4** (Network & Transport)
- A Virtual Private Network (or VPN for short) is a technology that allows devices on separate networks to communicate securely by creating a dedicated path between each other over the Internet (known as a tunnel). Devices connected within this tunnel form their own private network.

For example, only devices within the same network (such as within a business) can directly communicate. However, a VPN allows two offices to be connected. Let's take the diagram below, where there are three networks:

Network #1 (Office #1)
Network #2 (Office #2)
Network #3 (Two devices connected via a VPN)
The devices connected on Network #3 are still a part of Network #1 and Network #2 but also form together to create a private network (Network #3) that only devices that are connected via this VPN can communicate over.

Let's cover some of the other benefits offered by a VPN in the table below:

Benefit	Description
Allows networks in different geographical locations to be connected.	For example, a business with multiple offices will find VPNs beneficial, as it means that resources like servers/infrastructure can be accessed from another office.
Offers privacy.	
VPN technology uses encryption to protect data. This means that it can only be understood between the devices it was being sent from and is destined for, meaning the data isn't vulnerable to sniffing.

This encryption is useful in places with public WiFi, where no encryption is provided by the network. You can use a VPN to protect your traffic from being viewed by other people.

Offers anonymity.	
Journalists and activists depend upon VPNs to safely report on global issues in countries where freedom of speech is controlled.

Usually, your traffic can be viewed by your ISP and other intermediaries and, therefore, tracked. 

The level of anonymity a VPN provides is only as much as how other devices on the network respect privacy. For example, a VPN that logs all of your data/history is essentially the same as not using a VPN in this regard.

TryHackMe uses a VPN to connect you to our vulnerable machines without making them directly accessible on the Internet! This means that:
You can securely interact with our machines
Service providers such as ISPs don't think you are attacking another machine on the Internet (which could be against the terms of service)
The VPN provides security to TryHackMe as vulnerable machines are not accessible using the Internet.

VPN technology has improved over the years. Let's explore some existing VPN technologies below:

VPN Technology	Description
PPP	
This technology is used by PPTP (explained below) to allow for authentication and provide encryption of data. VPNs work by using a private key and public certificate (similar to SSH). A private key & certificate must match for you to connect.

This technology is not capable of leaving a network by itself (non-routable).

PPTP	
The Point-to-Point Tunneling Protocol (PPTP) is the technology that allows the data from PPP to travel and leave a network. 

PPTP is very easy to set up and is supported by most devices. It is, however, weakly encrypted in comparison to alternatives.

IPSec	
Internet Protocol Security (IPsec) encrypts data using the existing Internet Protocol (IP) framework.

IPSec is difficult to set up in comparison to alternatives; however, if successful, it boasts strong encryption and is also supported on many devices.
## What Firewalls Check
- where traffic comes from
- where traffic is going
- what port it targets
- whether it's TCP or UDP
- uses **packet inspection**

## Types of Firewalls

### Stateful
- uses info about the **entire connection**
- dynamic decisions
- blocks full connection if behavior is bad
- uses more resources

### Stateless
- checks **individual packets** only
- follows strict, static rules
- uses fewer resources
- good for large traffic events (ex: DDoS)

# VPNs (Virtual Private Networks)

- create a **secure, encrypted tunnel** over the Internet
- let devices on different networks communicate as if on the **same private network**
- used by businesses, remote workers, journalists, and also by TryHackMe for safe lab access

## What VPNs Do
- connect networks across distanc (ex: multiple offices)
- protect privacy with **encryption**
- offer some anonymity from ISPs/observers
- keep traffic hidden on insecure networks (ex: public WiFi)

## Why TryHackMe Uses a VPN
- lets you safely access vulnerable machines
- prevents ISPs from thinking you're attacking real hosts
- prevents THM machines from being exposed to the public Internet

## VPN Technologies

### PPP (Point-to-Point Protocol)
- provides **authentication + encryption**
- uses keys/certificates
- **not routable** on its own (can't leave the network))

### PPTP (Point-toPoint Tunneling Protocol)
- moves PPP traffic between networks
- very easy to set up
- **weak encryption**

### IPSec
- encrypts traffic using normal IP networking
- harder to configure
- **very strong encryption**

---

# Routers vs Switches

## Router
- connects **different networks** together
- moves packets using **routing** (Layer 3)
- chooses the best path based on:
  - shortest route
  - most reliable
  - fastest medium (copper vs fiber)
- has a management interface (web UI / console) for things like:
  - port forwarding
  - firewall rules
- **does NOT** do the same job as a switch

---

## Switch
- connects **multiple devices inside the same network**
- uses **Ethernet** to link machines (3-63+ ports)

### Layer 2 Switch
- works at **Layer 2**
- forwards **frames** using MAC addresses
- only handles local network traffic

### Layer 3 Switch
- works at **Layer 3**
- does everything a Layer 2 switch does **plus some routing**
- can route IP traffic between internal networks (VLANs)

---

## VLANs (Virtual LANs)
- split one physical switch into **separate virtual networks**
- devices share the same hardware but are **logically isolated**
- example
  - Sales and Accounting can both reach the Internet
  - but **cannot talk to each other**
- used for security + traffic control
