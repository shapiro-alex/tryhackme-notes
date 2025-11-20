# DNS in Detail (Domain Name System)

- matches **domain names -> IP addresses**
- makes the internet usable (humans remember words, not numbers)
- every device has a unique **IP address** (example: 104.26.10.229)
- DNS lets you visit a site using **tryhackme.com**, not its IP
- works like a "phone book" for the internet

---

## DNS Structure

**TLD (Top-Level Domain)**
- rightmost part (eample: `.com`)
- two types: **gTLD** (generic) and **ccTLD** (country code)
- gTLD = purpose (`.com`, `.org`, `.edu`)
- ccTLD = region (`.ca`, `.co.uk`)
- now many new gTLDs exist (`.online`, `.club`, `.biz`)

**Second-Level Domain**
- part before the TLD (example: `tryhackme` in `tryhackme.com`)
- up to 63 chars; a-z, 0-9, hyphens only
- cannot start/end with hypens or have consecutive hyphens

**Subdomain**
- left of the second-level domain (example: `admin.tryhackme.com`)
- same rules as SLD
- can chain multiple subdomains (`jupiter.servers.tryhackme.com`)
- total length ≤ 253 chars

---

##DNS Record Types

**A Record**
- maps a domain -> IPv4 address
- example: `104.26.10.229`

**AAAA Record**
- maps a domain -> IPv6 address
- example: `2606:4700:20::681a:be5`

**CNAME Record**
- alias that points a domain -> another domain
- example: `store.tryhackme.com` -> `shops.shopify.com`
- second lookup returns the actual IP

**MX Record**
- points to mail servers for a domain
- includes **priority** values (lower = tried first)
- example `alt1.aspmx.l.google.com`

**TXT Record**  
- free-form text data  
- used for SPF (email sender authority), domain verification, etc.

---

## What Happens During a DNS Request

**1. Check Local Cache**  
- your computer looks for a saved DNS result  
- if found → returned instantly  
- if not → sent to your **Recursive DNS Server**

**2. Recursive DNS Server Lookup**  
- usually provided by your ISP (or set to something like 1.1.1.1 / 8.8.8.8)  
- checks its own cache  
- if found → returned to you  
- if not → begins full DNS lookup

**3. Query Root DNS Servers**  
- root servers = backbone of DNS  
- job: direct the request to the correct **TLD server**  
- example: for `tryhackme.com`, root sends you to the **.com** TLD server

**4. Query TLD Server**  
- TLD server doesn’t know the IP  
- instead it knows **which nameserver is authoritative**  
- e.g., for `tryhackme.com`:  
  - `kip.ns.cloudflare.com`  
  - `uma.ns.cloudflare.com`

**5. Query Authoritative Nameserver**  
- stores the actual DNS records (A, AAAA, MX, CNAME, TXT, etc.)  
- returns the correct record (e.g., the IPv4 for `tryhackme.com`)

**6. Cache & Return**  
- recursive server caches result using the record’s **TTL** (Time To Live, in seconds)  
- sends the final answer back to your computer  
- your computer also caches it  
