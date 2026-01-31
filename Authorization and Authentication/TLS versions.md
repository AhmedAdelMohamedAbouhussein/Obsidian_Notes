## What is TLS?

**TLS (Transport Layer Security)** is a **security protocol** that provides:

- Encryption (confidentiality)
- Authentication (identity verification)
- Integrity (data not modified)

Used in:

- HTTPS
- HTTP/2
- HTTP/3 (via QUIC)
- Email, APIs, VPNs, gRPC

---

## TLS Version Timeline

|Version|Year|Status|
|---|---|---|
|SSL 1.0|1994|❌ Never released|
|SSL 2.0|1995|❌ Broken|
|SSL 3.0|1996|❌ Broken|
|TLS 1.0|1999|❌ Deprecated|
|TLS 1.1|2006|❌ Deprecated|
|**TLS 1.2**|2008|⚠️ Still widely used|
|**TLS 1.3**|2018|✅ Modern standard|

---

## TLS 1.0 & 1.1 (Deprecated)

### Why They’re Bad

- Weak cryptography
- Vulnerable to known attacks
- Slow handshakes
- No modern cipher support

### Status

- Disabled by browsers
- Not allowed by compliance standards

---

## TLS 1.2

### Why It Was Important

- Strong encryption
- Flexible cipher suites
- Secure for many years

### How It Works (High Level)

- Multiple RTTs for handshake
- Many cipher suite options
- More complexity

### Downsides

- Slower handshake
- Easy to misconfigure
- Large attack surface

### Still Used By

- Legacy systems
- Some APIs
- Enterprises with older infrastructure

---

## TLS 1.3 (Most Important)

### Why TLS 1.3 Exists

- Simplify security    
- Remove weak algorithms
- Improve performance
- Enable 0-RTT    

---

## Major Improvements in TLS 1.3

### 1. Faster Handshake

- TLS 1.2: **2 RTT**    
- TLS 1.3: **1 RTT**
- TLS 1.3 + 0-RTT: **0 RTT**

---

### 2. Stronger Security

Removed:

- RSA key exchange    
- Static Diffie-Hellman
- SHA-1
- CBC mode
- Compression (CRIME attack)

Only allows:

- Forward secrecy
- Modern AEAD ciphers    

---

### 3. Simpler Cipher Suites

**TLS 1.2**
`TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256`

**TLS 1.3**
`TLS_AES_128_GCM_SHA256`

Less confusion, fewer mistakes.

---

### 4. Encrypted Handshake

- More handshake messages encrypted    
- Harder to inspect or attack

---

## TLS 1.3 + 0-RTT

### What It Adds

- Returning clients send data immediately
- Used by HTTP/3 & QUIC    

### Limitation

- Replay attack risk
- Only safe for idempotent requests

---

## TLS 1.3 vs TLS 1.2 (Table)

| Feature         | TLS 1.2  | TLS 1.3   |
| --------------- | -------- | --------- |
| Handshake RTT   | 2        | 1         |
| 0-RTT           | ❌        | ✅         |
| Cipher suites   | Many     | Few       |
| Forward secrecy | Optional | Mandatory |
| Security        | Good     | Excellent |
| Performance     | Slower   | Faster    |

---

## TLS and HTTP Versions

| HTTP Version | TLS Version                |
| ------------ | -------------------------- |
| HTTP/1.1     | TLS 1.2 / 1.3              |
| HTTP/2       | TLS 1.2 / 1.3              |
| HTTP/3       | TLS 1.3 only (inside QUIC) |

---

## What Is Used Today (Real World)

✅ **TLS 1.3** – default and recommended  
⚠️ **TLS 1.2** – fallback / legacy  
❌ TLS 1.0 / 1.1 – disabled

---

## One-Paragraph Exam Answer

> TLS is a security protocol that provides encrypted and authenticated communication. Older versions such as TLS 1.0 and 1.1 are deprecated due to security weaknesses. TLS 1.2 improved security but has a slower and more complex handshake. TLS 1.3 simplifies the protocol, removes weak algorithms, reduces handshake latency, and supports 0-RTT, making it the modern standard used with HTTP/2 and HTTP/3.

---

## Memory Hooks

- TLS 1.2 → **secure but slow**
    
- TLS 1.3 → **secure + fast**
    
- HTTP/3 → **TLS 1.3 only**