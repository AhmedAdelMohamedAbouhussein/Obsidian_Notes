## What is gRPC?

**gRPC (Google Remote Procedure Call)** is a **high-performance communication framework** used to let different applications or services **call functions on each other over the network** as if they were local function calls.

Instead of sending plain HTTP requests manually, gRPC lets a client say:

> “Run this function on that server and give me the result.”

---

## Key Ideas

- **RPC (Remote Procedure Call):**  
    Call a method on another machine like a normal function.
    
- **Protocol Buffers (Protobuf):**  
    gRPC uses **Protobuf** to define data and services → compact, fast, strongly typed.
    
- **HTTP/2 based:**  
    Uses HTTP/2 under the hood → faster than REST (multiplexing, streaming, lower latency).
    

---

## How gRPC Works

1. You define a **service + methods** in a `.proto` file
    
2. gRPC generates **client & server code** automatically
    
3. Client calls a method
    
4. Server executes it and returns the response
    

➡️ No manual JSON, no parsing headaches.

---

## Example (Conceptual)

`service UserService {   rpc GetUser (UserRequest) returns (UserResponse); }`

Client calls `GetUser()` → server runs it → response comes back.

---

## gRPC vs REST (Quick Comparison)

|Feature|gRPC|REST|
|---|---|---|
|Protocol|HTTP/2|HTTP/1.1|
|Data format|Protobuf (binary)|JSON (text)|
|Speed|Very fast|Slower|
|Typing|Strongly typed|Loosely typed|
|Streaming|Built-in|Limited|
|Browser friendly|❌ (needs proxy)|✅|

---

## When to Use gRPC

✅ Microservices  
✅ Internal service-to-service communication  
✅ Low latency systems  
✅ Real-time streaming (chat, telemetry)

❌ Public APIs for browsers (REST is easier)

---

## Languages Supported

gRPC supports many languages:

- Java
- C++
- Python
- Go
- C#
- Node.js

---

## One-Line Summary 

> gRPC is a fast, strongly-typed RPC framework by Google that uses HTTP/2 and Protocol Buffers for efficient communication between distributed systems.