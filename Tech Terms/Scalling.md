Scaling is **increasing a system’s capacity** to handle more load, traffic, or data. There are two main types: **Vertical Scaling** and **Horizontal Scaling**.

---

## 1. Vertical Scaling (Scale Up)

**Meaning:**

- Add more **resources to a single server** (CPU, RAM, disk).
- Makes one machine **more powerful**.

**Pros:**

- Simple to implement
- No changes to application architecture

**Cons:**

- Limited by hardware
- Single point of failure

**Example:**

- Upgrading a database server from 16GB → 64GB RAM
- Replacing a CPU with a faster model

**Memory Hook:**

- “**Make one machine stronger**”

---

## 2. Horizontal Scaling (Scale Out)

**Meaning:**

- Add **more servers or nodes** to the system.    
- Distribute load across multiple machines.

**Pros:**

- Virtually unlimited scaling
- Fault-tolerant (if one node fails, others continue)

**Cons:**

- More complex (needs load balancers, distributed systems)
- Data consistency and replication needed

**Example:**

- Adding more web servers behind a load balancer
- Splitting a database into shards across multiple machines

**Memory Hook:**

- “**Add more machines instead of making one stronger**”    

---

## 3. Comparison Table

| Feature         | Vertical Scaling              | Horizontal Scaling              |
| --------------- | ----------------------------- | ------------------------------- |
| How             | Add resources to one machine  | Add more machines/nodes         |
| Complexity      | Low                           | High                            |
| Fault Tolerance | Low (single point of failure) | High                            |
| Limit           | Hardware limit                | Practically unlimited           |
| Example         | Bigger CPU/RAM                | Multiple web servers, DB shards |

---

## 4. One-Line Exam Answer

> Vertical scaling increases the resources of a single machine, while horizontal scaling adds more machines to distribute the load across the system.