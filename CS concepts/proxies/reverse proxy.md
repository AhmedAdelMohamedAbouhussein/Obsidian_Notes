## 🔹 What is a Reverse Proxy?

- A **reverse proxy** sits **in front of servers**, not clients.
    
- Instead of protecting _users_, it protects and manages access to _servers_.
    
- When a client (browser, app, etc.) makes a request, it goes to the **reverse proxy first**. The proxy then decides which server should handle the request.

So the **client never talks directly to your backend servers** — only to the reverse proxy.

---

## 🔹 Uses of Reverse Proxy

1. **Load balancing**
    
    - Distributes incoming traffic across multiple backend servers.
    - Example: If you have 5 Node.js servers running, the reverse proxy spreads requests among them.
        
2. **Security**
    
    - Hides your servers’ real IP addresses.
    - Acts as a first line of defense against DDoS or malicious requests.
        
3. **SSL/TLS termination**
    
    - The reverse proxy handles HTTPS (certificates, encryption) so backend servers only deal with plain HTTP.
        
4. **Caching & compression**
    
    - Stores frequently accessed static content (images, CSS, JS) and compresses responses to improve performance.
        
5. **Centralized routing**
    
    - Lets you route requests to different microservices.
    - Example:
        - `/api/users` → User service
        - `/api/payments` → Payments service
        - `/static/*` → Static file server

---

## 🔹 Example Flow

Say your frontend calls your backend at `api.myapp.com`:

1. The client request → **reverse proxy** (e.g., Nginx, HAProxy, or AWS ALB).
    
2. Proxy forwards the request to one of your backend servers (say Node.js on port 5000).
    
3. Server responds → proxy → client.
    

The client **never knows about your internal servers**.

---

✅ **Forward proxy = hides the client from the server.**  
✅ **Reverse proxy = hides the server(s) from the client.**