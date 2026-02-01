Here’s a **clear, concise, system-design level explanation of Idempotency** — perfect for notes or interviews:

---

# **Idempotency**

### Definition

**Idempotency** is a property of an operation where **performing it multiple times has the same effect as performing it once**.

> In simple terms: **“No matter how many times you repeat it, the outcome is the same.”**

---

### Why It Matters

- Ensures **safe retries** in distributed systems, network failures, or crashes.
    
- Prevents **duplicate transactions** (e.g., double payments).
    
- Important in **REST APIs, caching, and message processing**.
    

---

### Examples

**1️⃣ HTTP Methods**

- **GET** → idempotent (reading data multiple times doesn’t change it)
    
- **PUT** → idempotent (updating a resource to the same value multiple times is safe)
    
- **DELETE** → idempotent (deleting the same resource multiple times has the same effect)
    
- **POST** → usually **not idempotent** (creating a new resource multiple times creates duplicates)
    

**2️⃣ Payments**

- If a payment request is retried due to network error, using an **idempotency key** ensures only **one payment** is processed.
    

---

### How to Achieve Idempotency

1. **Idempotency Keys**
    
    - Client sends a unique key with a request.
        
    - Server stores processed keys to **prevent duplicate processing**.
        
2. **Design Operations Carefully**
    
    - E.g., `balance = 100` → setting it multiple times is safe.
        
    - Avoid operations like `balance += 100` without checks.
        
3. **Stateless Services**
    
    - If services don’t rely on mutable state, operations are naturally idempotent.
        

---

### Pros

- Safer retries
    
- Prevents duplicate work
    
- Improves reliability in distributed systems
    

### Cons / Challenges

- Requires **tracking keys or state**
    
- Extra **storage overhead**
    
- Not all operations can be made idempotent easily
    

---

### One-line Definition (exam-friendly)

> **Idempotency is when repeating an operation produces the same result as doing it once, ensuring safety for retries.**