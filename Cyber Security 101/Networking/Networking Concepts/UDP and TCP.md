## Transport Layer Summary (UDP vs TCP)

**IP** identifies the destination **host** using an IP address.  
**Transport protocols** identify the **process** on that host using **port numbers**.

- **Port range:** 1–65535 (port 0 reserved)
- **Layer:** Transport Layer (Layer 4)
- **Main protocols:** UDP and TCP

---

### UDP (User Datagram Protocol)
- **Type:** Connectionless
- **Reliability:** No delivery confirmation
- **Speed:** Fast, low overhead
- **Use case:** When speed matters more than reliability
- **Analogy:** Sending mail with no delivery receipt
- **Key traits:**
  - No connection setup
  - No acknowledgements
  - No guarantee packets arrive or arrive in order

---

### TCP (Transmission Control Protocol)
- **Type:** Connection-oriented
- **Reliability:** Guaranteed delivery and ordering
- **Speed:** Slower than UDP due to overhead
- **Use case:** When reliability matters
- **Key traits:**
  - Requires connection establishment
  - Uses sequence numbers and acknowledgements
  - Detects lost or duplicated packets

---

### TCP Three-Way Handshake
1. **SYN:** Client requests a connection and sends initial sequence number
2. **SYN-ACK:** Server acknowledges and sends its own sequence number
3. **ACK:** Client acknowledges, connection established
