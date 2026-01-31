### Meaning

**WebSockets** is a protocol that enables **full-duplex, real-time communication** between a client (browser) and a server over a single TCP connection.

- Unlike HTTP, which is **request-response**, WebSockets allow **both sides to send data anytime**.

---

## 1. How WebSockets Work

1. **Handshake:**
    
    - Client sends an HTTP request with `Upgrade: websocket`.        
    - Server responds and upgrades the connection to WebSocket.
        
2. **Persistent Connection:**
    
    - Single TCP connection remains open.
    - Messages can flow **bi-directionally** in real-time.
        
3. **Close Connection:**
    
    - Either side can terminate when done.        

---

## 2. Key Features

- **Full-duplex:** Both client & server can send messages simultaneously.    
- **Low latency:** No need to establish a new connection for each message.
- **Lightweight:** Minimal headers after handshake.
- **Stateful:** Connection stays open.

---

## 3. Use Cases

- Real-time chat apps (e.g., WhatsApp Web, Slack)    
- Live notifications & feeds
- Multiplayer online games
- Collaborative editing (e.g., Google Docs)    
- Financial tickers / stock updates

---

## 4. Comparison to HTTP

| Feature       | HTTP                | WebSocket                    |
| ------------- | ------------------- | ---------------------------- |
| Communication | Request → Response  | Bi-directional (full-duplex) |
| Connection    | New TCP per request | Single persistent TCP        |
| Latency       | Higher              | Low                          |
| Real-time     | Harder              | Easy                         |
| Headers       | Larger              | Minimal after handshake      |

---

## 5. Memory Hook

- Think: **“WebSocket = always-open chat line between client & server”**    

---

## 6. One-Line Exam Answer

> WebSockets is a protocol that provides a persistent, full-duplex connection between client and server, allowing real-time, low-latency communication.