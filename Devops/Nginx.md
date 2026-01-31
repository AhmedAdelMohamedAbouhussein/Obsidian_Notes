It’s a **software** you install on a **server you manage** (like a VPS or cloud instance). Not a hosting platform.

## 1. Introduction

**Nginx** (pronounced _engine-x_) is a **high-performance web server**, **reverse proxy**, and **load balancer**.  
It was created by **Igor Sysoev** in 2004 and is widely used for:

- Serving static content
- Load balancing
- Reverse proxying
- Caching
- Handling high concurrency

---

## 2. Key Features

- **Event-driven, asynchronous architecture** → handles thousands of connections with low memory
- **Reverse proxy** → forwards client requests to backend servers
- **Load balancing** → distributes requests across multiple servers
- **Caching** → speeds up static content delivery
- **SSL/TLS termination** → secure HTTPS
- **HTTP/2 support** → faster modern web protocols
- **WebSockets support** → real-time applications

---

## 3. Nginx Architecture

Nginx uses a **master-worker model**:

### 3.1 Master Process

- Starts and manages worker processes
- Reads configuration files
- Handles signals (reload, shutdown)

### 3.2 Worker Processes

- Handle **client connections**
- Process requests asynchronously using an **event loop**
- Can serve thousands of simultaneous clients

---

## 4. Nginx as a Web Server

- Handles **HTTP requests** directly
- Serves **static files** efficiently
- Can run **dynamic content** using FastCGI (e.g., PHP, Python)

### Example: Serving Static Files
![[Pasted image 20251218153448.png]]
## 5. Nginx as a Reverse Proxy

- Receives client requests
- Forwards them to one or more backend servers
- Returns the backend’s response to the client

### Example
![[Pasted image 20251218153501.png]]

## 6. Load Balancing

- Distributes requests across multiple servers
- Supports **round-robin**, **least connections**, **IP hash**

### Example: Round-Robin
![[Pasted image 20251218153521.png]]

## 7. Caching

- Nginx can **cache responses** from backend servers
- Reduces load and improves speed

### Example
![[Pasted image 20251218153532.png]]

## 8. SSL/TLS (HTTPS)

- Nginx handles **HTTPS connections**
- Can terminate SSL at the proxy (backend receives plain HTTP)

### Example
![[Pasted image 20251218153607.png]]
## 9. URL Rewriting & Redirection

- Nginx can **rewrite URLs** or redirect requests

### Example

![[Pasted image 20251218153622.png]]
## 10. Nginx Configuration Structure

![[Pasted image 20251218153637.png]]
### Key Directives

- `listen` → port
- `server_name` → domain
- `location` → URL path
- `root` → file location
- `proxy_pass` → backend server

---

## 11. Logging

- **Access log** → records all requests
- **Error log** → records errors

![[Pasted image 20251218153658.png]]
## 12. Advantages

- High performance (asynchronous)
- Handles **thousands of concurrent connections**
- Lightweight, low memory usage
- Easy to configure for web server, proxy, or load balancer
- Widely supported, open-source

---

## 13. Common Nginx Commands

![[Pasted image 20251218153721.png]]

## 14. Nginx vs Apache

|Feature|Nginx|Apache|
|---|---|---|
|Architecture|Event-driven|Process/thread|
|Performance|High|Moderate|
|Static content|Excellent|Good|
|Dynamic content|Needs FastCGI|Built-in modules|
|Memory usage|Low|High|
|Concurrency|Thousands|Hundreds|
## 15. Nginx Use Cases

- Web server for static and dynamic content
    
- Reverse proxy for microservices
    
- Load balancer for high-availability systems
    
- SSL termination for HTTPS
    
- API gateway
    

---

## 16. Summary

- **Nginx** = high-performance web server + reverse proxy + load balancer
    
- **Event-driven architecture** = handles thousands of connections efficiently
    
- Can serve **static content**, proxy to **backends**, load balance, cache, and secure connections
    
- Essential for **modern web and microservices architecture**