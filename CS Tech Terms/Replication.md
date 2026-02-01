### Meaning

**Replication** is the process of **copying data from one database (master/primary) to one or more other databases (replicas/secondaries)** to improve **availability, reliability, and performance**.

- Ensures **multiple copies of the same data** exist.
    
- Common in **distributed systems** and large-scale databases.
    

---

## 1. How Replication Works

1. **Primary-Secondary (Master-Slave) Replication**
    
    - Primary handles **writes**
        
    - Secondary replicas **copy data** from primary
        
    - Reads can be distributed to replicas
        
2. **Multi-Master Replication**
    
    - Multiple nodes can **accept writes**
        
    - Data is synchronized across all nodes
        
3. **Asynchronous vs Synchronous**
    
    - **Asynchronous:** replicas update a little later → faster, may lag
        
    - **Synchronous:** replicas update immediately → slower, always consistent
        

---

## 2. Why Replication is Used

- **High availability:** if one server fails, replicas take over
    
- **Load balancing:** read-heavy apps can use replicas
    
- **Disaster recovery:** data backup across multiple nodes
    
- **Geographical distribution:** closer replicas → faster access
    

---

## 3. Examples

- MySQL: master-slave replication
    
- MongoDB: replica sets
    
- Cassandra: automatic replication across nodes
    

---

## 4. Memory Hook

- Think: **“Make copies of the database to stay safe, fast, and available”**
    
- Replication = “cloning data across servers”
    

---

## 5. One-Line Exam Answer

> Replication is the process of copying data from a primary database to one or more replicas to ensure availability, reliability, and performance.