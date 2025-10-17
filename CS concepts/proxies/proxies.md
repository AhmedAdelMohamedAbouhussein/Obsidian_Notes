## 🔹 1. Based on **anonymity level**

1. **Transparent Proxy**
    
    - Forwards your IP to the server.
    - Does not provide privacy.
    - Often used in corporate networks, schools, or ISPs.
        
2. **Anonymous Proxy**
    
    - Hides your real IP, but identifies itself as a proxy.
    - Provides some privacy, but the server knows you’re using a proxy.
        
3. **Elite / High Anonymity Proxy**
    
    - Hides your IP and doesn’t reveal that you’re using a proxy.
    - Best for privacy and bypassing restrictions.

---

## 🔹 2. Based on **traffic direction**

1. **Forward Proxy**
    
    - Sits between the client and the internet.
    - You configure your device/app to use it.
    - Common use: bypass restrictions, caching.
        
2. **Reverse Proxy**
    
    - Sits in front of servers, not clients.
    - Clients don’t know it’s there.
    - Used for load balancing, caching, SSL termination, hiding server identity.
    - Example: **Nginx, HAProxy, Cloudflare**.

---

## 🔹 3. Based on **protocol**

1. **HTTP Proxy** – handles HTTP traffic only.

2. **HTTPS Proxy** – handles encrypted HTTPS traffic.

3. **SOCKS Proxy (SOCKS4, SOCKS5)** – more general, works with any protocol (HTTP, FTP, SMTP, etc.). SOCKS5 supports authentication.

4. **FTP Proxy** – specialized for file transfers.

---

## 🔹 4. Based on **application**

1. **Residential Proxy** – uses IPs from real residential devices (looks like normal users).
    
2. **Datacenter Proxy** – uses IPs from data centers (fast but easier to detect).
    
3. **Mobile Proxy** – uses IPs from mobile carriers (harder to block).

---

## 🔹 5. Special types

- **Transparent Caching Proxy** – caches frequently used data to reduce bandwidth.
    
- **CGI Proxy (Web-based proxy)** – accessed via a website (e.g., free proxy sites).
    
- **Rotating Proxy** – automatically changes IPs from a pool.
    
- **Open Proxy** – available to anyone (often unsafe, can be malicious).

---

✅ **Summary**:

- By anonymity → Transparent, Anonymous, Elite.
    
- By direction → Forward, Reverse.
    
- By protocol → HTTP, HTTPS, SOCKS, FTP.
    
- By application → Residential, Datacenter, Mobile.
    
- Special flavors → Rotating, Web-based, etc.