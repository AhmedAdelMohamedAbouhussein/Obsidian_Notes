## 1. HTTP/1.1

### What it is

The classic, text-based version of HTTP used for decades.  
Runs on **TCP**.

### Key Characteristics

- Text-based protocol
- One request per connection (mostly)
- Head-of-line blocking
- Multiple TCP connections per site
- No built-in multiplexing

### Who Uses HTTP/1.1 Today

- Older servers and legacy systems
- Simple websites
- Systems where HTTP/2 is not enabled
- Some internal or embedded systems

### Still Used Because

- Extremely compatible
- Simple to debug
- Universally supported

---

## 2. HTTP/2

### What it is

A performance upgrade to HTTP/1.1 that keeps the same HTTP semantics but improves **how data is sent**.  
Runs on **TCP (with TLS in practice)**.

### Key Characteristics

- Binary protocol
- Multiplexing (parallel requests)
- Header compression (HPACK)
- Single TCP connection
- Optional server push

### Who Uses HTTP/2

- Modern browsers (Chrome, Firefox, Edge, Safari)
- Most major websites
- REST APIs
- Microservices communication
- gRPC (mandatory)

### Used By

- Google
- YouTube
- GitHub
- AWS / Azure / Cloudflare
- Mobile & web apps

### Why It’s Popular

- Faster page loads
- Lower latenc    
- Efficient for many small requests

---

## 3. HTTP/3 (NEWEST)

### What it is

The newest HTTP version designed to **fix TCP limitations**.  
Runs on **QUIC over UDP**, not TCP.

### Key Characteristics

- Uses **UDP + QUIC**    
- No TCP head-of-line blocking
- Faster connection setup (0-RTT)
- Built-in encryption
- Better performance on bad networks (Wi-Fi, mobile)

### Why HTTP/3 Exists

Even HTTP/2 still suffers from:

- **TCP-level head-of-line blocking**  
    If one packet is lost → everything waits.

HTTP/3 removes this by **not using TCP at all**.

---

## Who Uses HTTP/3

### Heavy Real-Time & Mobile Apps

- Google Search    
- YouTube
- Google Drive
- Facebook / Meta
- Cloudflare-powered sites
- Mobile apps with unstable networks

### Best For

- Mobile networks
    
- High-latency or lossy connections
    
- Real-time apps
    
- Streaming and gaming platforms
    

---

## 4. Comparison Table

|Feature|HTTP/1.1|HTTP/2|HTTP/3|
|---|---|---|---|
|Transport|TCP|TCP|UDP (QUIC)|
|Data format|Text|Binary|Binary|
|Multiplexing|❌|✅|✅|
|Head-of-line blocking|❌ Yes|⚠️ TCP-level|❌ No|
|Header compression|❌|✅|✅|
|Encryption|Optional|Practically required|Mandatory|
|Mobile performance|❌ Poor|✅ Good|✅ Excellent|

---

## 5. Which One Should Be Used?

### Use HTTP/1.1 when:

- Legacy compatibility is required
    
- Simple systems
    
- Debugging simplicity matters
    

### Use HTTP/2 when:

- Building modern websites
    
- REST APIs
    
- Microservices
    
- gRPC communication
    

### Use HTTP/3 when:

- Mobile-first apps
    
- Real-time systems
    
- High packet loss environments
    
- Performance is critical
    

---

## 6. One-Line Exam Summary

> HTTP/1.1 is the original text-based protocol, HTTP/2 improves performance using multiplexing over TCP, and HTTP/3 further improves reliability and latency by using QUIC over UDP.

---

## 7. Mental Model (Easy to Remember)

- HTTP/1.1 → **many slow lanes**
    
- HTTP/2 → **many fast lanes in one tunnel**
    
- HTTP/3 → **new tunnel that avoids traffic jams**