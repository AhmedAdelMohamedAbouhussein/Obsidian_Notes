## What is a Load Balancer?

A **load balancer** distributes incoming client requests across **multiple backend servers** to ensure:

- High availability
    
- Scalability
    
- Better performance
    
- Fault tolerance
    

---

## Basic Architecture

![[Pasted image 20260201212309.png]]

## Why Load Balancers Are Needed

- Prevents server overload
    
- Eliminates single point of failure
    
- Enables horizontal scaling
    
- Improves response time
    
- Automatically handles server failures
    

---

## Types of Load Balancers

### 1️⃣ By OSI Layer

### Layer 4 (Transport Layer)

- Routes traffic using **IP address + port**
    
- Protocols: TCP, UDP
    
- Fast, low overhead
    
- Cannot inspect request content
    

**Examples:** HAProxy (L4), NGINX (L4), AWS NLB

---

### Layer 7 (Application Layer)

- Routes based on **HTTP/HTTPS data**
    
- Can route using:
    
    - URL path (`/api/users`)
        
    - Headers
        
    - Cookies
        
    - Hostnames
        
- More flexible, slightly slower
    

**Examples:** NGINX, AWS ALB, Envoy

---

### 2️⃣ By Deployment

- **Hardware Load Balancer** – expensive, enterprise-grade
    
- **Software Load Balancer** – most common (NGINX, HAProxy)
    
- **Cloud Load Balancer** – managed (AWS, Azure, GCP)
    

---

## Routing / Load-Balancing Algorithms

### 1️⃣ Round Robin

**How it works:**  
Requests are sent to servers **in order**, one by one.
![[Pasted image 20260201212332.png]]

### 2️⃣ Weighted Round Robin

**How it works:**  
Servers get traffic **based on assigned weight**.

![[Pasted image 20260201212409.png]]

**Pros:** Accounts for server power  
**Cons:** Static weights  
**Best for:** Mixed hardware servers

---

### 3️⃣ Least Connections

**How it works:**  
Request goes to the server with the **fewest active connections**.

**Pros:** Dynamic, adapts to load  
**Cons:** Slight overhead  
**Best for:** Long-lived connections

---

### 4️⃣ Weighted Least Connections

**How it works:**  
Least connections **plus server weight**.

**Pros:** Very accurate load distribution  
**Cons:** More complex  
**Best for:** Unequal servers with heavy traffic

---

### 5️⃣ IP Hash

**How it works:**  
Client IP is hashed → mapped to a server.

`Client IP → Hash → Server`

Pros: Session persistence
Cons: Uneven load if IPs are skewed
Best for: Stateful apps without shared session store

### 6️⃣ URL Hash

**How it works:**  
Routes requests based on **URL**.

`/images → Server A`
`/videos → Server B`

**Pros:** Cache-friendly  
**Cons:** Can overload popular URLs  
**Best for:** Content delivery systems

---

### 7️⃣ Least Response Time

**How it works:**  
Routes to the server with:

- Fewest connections
    
- Fastest response time
    

**Pros:** Performance optimized  
**Cons:** Needs monitoring  
**Best for:** Latency-sensitive apps

---

### 8️⃣ Random

**How it works:**  
Random server selection.

**Pros:** Simple  
**Cons:** Poor predictability  
**Best for:** Rare / testing scenarios

---

### 9️⃣ Consistent Hashing

**How it works:**  
Minimizes request reassignment when servers are added/removed.

**Pros:** Stable routing  
**Cons:** Complex  
**Best for:** Distributed caches (Redis, Memcached)

---

## Health Checks

Load balancer checks backend servers using:

- HTTP status checks (200 OK)
    
- TCP checks
    
- Custom endpoints (`/health`)
    

Unhealthy servers are **removed automatically**.

---

## Sticky Sessions (Session Persistence)

Ensures a client is routed to the **same server**:

- Cookies
    
- IP hashing
    

⚠️ Reduces scalability  
✅ Better solution: shared session store (Redis)

---

## Load Balancer in Microservices

- Sits before:
    
    - API Gateway
        
    - Individual services
        
- Enables independent service scaling
    

`Client → Load Balancer → API Gateway → Services`

---

## Advantages

- Improves uptime
    
- Better traffic distribution
    
- Enables fault tolerance
    
- Supports scaling
    

---

## Disadvantages

- Extra cost
    
- Added latency
    
- Needs redundancy
    
- Configuration complexity
    

---

## Avoiding Load Balancer Failure

- Multiple load balancers
    
- Active-active setup
    
- DNS-based failover
    

---

## Popular Load Balancers

- NGINX
- HAProxy
- Envoy    
- AWS ALB / NLB
- Cloudflare

## One-Line Exam Answer ✅

> A load balancer distributes incoming traffic across multiple servers using routing algorithms to improve performance, availability, and scalability.