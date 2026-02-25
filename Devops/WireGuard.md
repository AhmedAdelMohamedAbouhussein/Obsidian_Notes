## 1️⃣ Definition

**WireGuard** is a **modern VPN protocol and software** designed to:

- Provide **secure point-to-point connections**
    
- Be **faster, simpler, and more efficient** than traditional VPNs (like OpenVPN or IPSec)
    
- Use **state-of-the-art cryptography**
    

Key goals:

- Simplicity (≤ 4,000 lines of code)
    
- High performance (fast encryption/decryption)
    
- Easy to configure and audit
    

---

## 2️⃣ How WireGuard Works

WireGuard operates **at the network layer (Layer 3)**:

- Creates **encrypted tunnels** between peers
    
- Each peer has a **public/private key pair**
    
- Traffic is routed securely using **cryptokey routing**
    

Steps:

1. Each peer generates a **key pair** (private + public)
    
2. Each peer is configured with:
    
    - Its own private key
        
    - Allowed IPs for the peer
        
    - Peer’s public key and endpoint (IP:port)
        
3. WireGuard encrypts traffic using **Noise protocol framework**
    
4. Only traffic to **configured Allowed IPs** is routed through the tunnel
    

---

## 3️⃣ Key Features

|Feature|Description|
|---|---|
|Encryption|Uses **modern cryptography** (ChaCha20, Curve25519, Poly1305, BLAKE2s, SipHash24)|
|Performance|Extremely fast, low latency, minimal CPU usage|
|Simplicity|Small codebase → easier to audit|
|Cross-platform|Linux, Windows, macOS, Android, iOS, routers|
|Stateless|Uses **UDP**, no handshake for idle peers|

---

## 4️⃣ Architecture / Concepts

1. **Peers**: Devices connected over the VPN
    
2. **Key pairs**: Each peer has a private/public key
    
3. **Allowed IPs**: Defines which IPs are routed through the tunnel
    
4. **Endpoints**: Public IP + port of remote peers
    
5. **Handshake**:
    
    - WireGuard uses **UDP handshake packets**
        
    - Establishes ephemeral session keys using Curve25519
        

---

## 5️⃣ Example Configuration (Linux)
![[{88856ACB-58BB-4052-9528-16E2C3EE68CE}.png]]
## 6️⃣ Cryptography Used

- **Key Exchange:** Curve25519
    
- **Symmetric Encryption:** ChaCha20
    
- **Message Authentication:** Poly1305
    
- **Hashing:** BLAKE2s
    
- **Packet IDs:** SipHash24
    

**Advantages:** Modern, secure, resistant to known attacks, simpler than IPSec.

---

## 7️⃣ Advantages

1. High performance (low CPU, high throughput)
    
2. Minimal configuration and dependencies
    
3. Secure and easy to audit
    
4. Works on **mobile and embedded devices**
    
5. Stateless → better NAT traversal
    

---

## 8️⃣ Limitations

1. **UDP only** → some networks block UDP
    
2. **No built-in authentication** → must trust peer keys
    
3. **New protocol** → fewer enterprise features than IPSec/OpenVPN
    
4. Works **best as point-to-point or site-to-site**, not full-featured enterprise VPN
    

---

## 9️⃣ Use Cases

- **Remote Access VPN** → connect laptop/mobile to home or office
    
- **Site-to-Site VPN** → connect two networks securely
    
- **IoT Security** → lightweight and fast encryption for devices
    
- **Cloud Network Tunneling** → connect cloud servers securely