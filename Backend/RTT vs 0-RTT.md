## What is RTT?

**RTT (Round-Trip Time)**  
= the time it takes for a message to go **client → server → client**

Used to measure **network latency**.

Example:

- Client sends “hello”
- Server replies “ok”    
- That round trip = **1 RTT**

---

## Normal RTT (Traditional Connection Setup)

### What happens (TCP + TLS example)

Before **any real data** is sent, several handshakes are needed.

### Steps:

1. **TCP handshake** (1 RTT)    
    - SYN → SYN-ACK → ACK
    
2. **TLS handshake** (1–2 RTTs)
    - Key exchange    
    - Certificate verification
        
3. **HTTP request/response** (1 RTT)

➡️ Total before data:

- **2–3 RTTs** just to start talking    

---

### Timeline (Normal RTT)

`Client → Server : SYN Server → Client : SYN-ACK Client → Server : ACK        (1 RTT)  Client → Server : TLS hello Server → Client : TLS reply  (2 RTTs)  Client → Server : HTTP request Server → Client : Response   (3 RTTs)`

---

## What is 0-RTT?

**0-RTT (Zero Round-Trip Time)** allows the client to send **application data immediately**, **without waiting** for the handshake to finish.

Used in:

- **TLS 1.3**
- **QUIC / HTTP/3**

---

## How 0-RTT Works

⚠️ Important: **only works for returning clients**

### First connection (no 0-RTT)

- Normal handshake    
- Server gives the client a **session ticket**

### Later connection (0-RTT)

- Client:
    - Reuses session info
    - Sends **data in the first packet**
        
- Server:
    - Accepts data immediately

➡️ No waiting = faster load time

---

## Timeline (0-RTT)

`Client → Server : Data + handshake info Server → Client : Response`

➡️ **Data sent immediately**

---

## RTT vs 0-RTT Comparison

| Feature               | Normal RTT       | 0-RTT          |
| --------------------- | ---------------- | -------------- |
| Handshake wait        | Yes              | No             |
| Data sent immediately | ❌                | ✅              |
| Latency               | Higher           | Lower          |
| First connection      | Required         | ❌              |
| Returning clients     | ❌                | ✅              |
| Used in               | TCP + TLS 1.2    | TLS 1.3 / QUIC |
| HTTP version          | HTTP/1.1, HTTP/2 | HTTP/3         |

---

## Why 0-RTT Is Faster

- Removes handshake delay
    
- Huge win on:
    
    - Mobile networks
    - High-latency connections
    - Global services

Example:

- Normal: 300–600 ms before data
- 0-RTT: data sent instantly

---

## Security Tradeoff (Important)

⚠️ **0-RTT is vulnerable to replay attacks**

Because:
- Server hasn’t fully verified client yet
- Attacker could replay the same request

### Therefore:

- 0-RTT is **only allowed for safe requests**
    - GET
    - Idempotent operations
        
- NOT recommended for:
    - Payments
    - State-changing actions

---

## Real-World Usage

### Uses 0-RTT

- HTTP/3
- QUIC
- Google services
- Cloudflare
- CDNs
- Mobile apps

### Does NOT use 0-RTT

- First-time connections
- Sensitive operations

---

## One-Paragraph Exam Answer

> RTT represents the time needed for a request to travel from client to server and back. In normal connections, several RTTs are required for TCP and TLS handshakes before data can be sent. 0-RTT allows a returning client to send application data immediately during connection setup, reducing latency significantly, and is used in TLS 1.3 and HTTP/3, although it introduces replay attack risks.

---

## Memory Hook

- Normal RTT → **wait, then send**
    
- 0-RTT → **send immediately**