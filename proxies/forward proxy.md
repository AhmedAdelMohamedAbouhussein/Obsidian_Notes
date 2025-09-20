A **forward proxy** is the "classic" type of proxy most people mean when they say _proxy_.

### 🔹 What it is

- A **forward proxy** sits **between a client (you)** and the **internet**.
- When you make a request to a website, the request goes **through the proxy** first.
- The proxy then forwards the request to the destination server **on your behalf**, and when the server responds, the proxy sends the response back to you.

So the **server never sees your real client directly**—it only sees the proxy.

---

### 🔹 Uses

1. **Privacy & anonymity**
    
    - Hides the client’s real IP address from the server.
    - Example: browsing via a corporate proxy or a VPN.
        
2. **Access control**
    
    - Companies can block certain websites (e.g., social media) by routing all traffic through a forward proxy.
        
3. **Caching**
    
    - A proxy can store frequently requested responses (like software updates), reducing bandwidth.
        
4. **Logging & monitoring**
    
    - Organizations use it to monitor employees’ internet usage.
        

---

### 🔹 Example Flow

Let’s say you (client) want to visit `example.com`:

1. Your browser sends a request to the **forward proxy**.
    
2. The proxy makes the request to `example.com` **on your behalf**.
    
3. `example.com` replies to the proxy.
    
4. The proxy returns the response back to you.

`example.com` sees the **proxy’s IP**, not yours.