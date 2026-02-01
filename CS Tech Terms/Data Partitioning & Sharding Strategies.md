## 1️⃣ Range-Based Partitioning

- **How it works:** Data is split based on key **ranges**.  
    Example: `user_id 1–1000 → Shard A`, `1001–2000 → Shard B`.
    
- **Pros:** Simple, predictable, good for range queries.
    
- **Cons:** Hotspot problem (if some ranges get more traffic), hard to rebalance.
    

---

## 2️⃣ Hash-Based Partitioning

- **How it works:** Apply a **hash function** to the key and map it to a shard.  
    Example: `hash(user_id) % 3 → Shard 0,1,2`.
    
- **Pros:** Even data distribution, easy to scale.
    
- **Cons:** Adding/removing shards requires **rehashing** (data reshuffling).
    

---

## 3️⃣ Directory-Based Partitioning

- **How it works:** Maintain a **directory (lookup table)** mapping keys to shards.
    
- **Pros:** Flexible, easy to rebalance, precise placement control.
    
- **Cons:** Directory can be a **single point of failure**, adds lookup latency.
    

---

## 4️⃣ Composite / Key-Based Partitioning

- **How it works:** Use **multiple keys** or fields for partitioning.  
    Example: Partition by `(country, user_id)` → `Shard(country, hash(user_id))`.
    
- **Pros:** Fine-grained control, avoids hotspots.
    
- **Cons:** More complex routing, harder to maintain.
    

---

## 5️⃣ Consistent Hashing

- **How it works:** Keys are mapped to a **hash ring**. When adding/removing shards, only a small portion of keys need remapping.
    
- **Pros:** Very scalable, minimal reshuffling, good for dynamic environments.
    
- **Cons:** Slightly more complex to implement.
    

---

## 6️⃣ Geographical / Location-Based Partitioning

- **How it works:** Partition data by **geography or region**.  
    Example: Users in EU → Shard A, Users in US → Shard B.
    
- **Pros:** Reduces latency for regional clients, legal compliance (data residency).
    
- **Cons:** Uneven distribution if traffic is uneven across regions.
    

---

## 7️⃣ Hybrid Partitioning

- **How it works:** Combine multiple strategies.  
    Example: **Range + Hash**, **Geo + Hash**, etc.
    
- **Pros:** Combines advantages of multiple methods, solves hotspots.
    
- **Cons:** Adds complexity.
    

---

## **Comparison Table**

| Strategy                  | How it Works                  | Pros                                    | Cons                                   | Best Use Case                           |
| ------------------------- | ----------------------------- | --------------------------------------- | -------------------------------------- | --------------------------------------- |
| **Range**                 | Split by key ranges           | Simple, predictable, easy range queries | Hotspots, hard to rebalance            | Sequential IDs, time-series data        |
| **Hash**                  | Hash(key) → shard             | Even distribution, easy to scale        | Rehashing needed on shard change       | Uniform load apps                       |
| **Directory**             | Directory lookup → shard      | Flexible, easy to rebalance             | Single point of failure, extra latency | Dynamic data placement                  |
| **Composite / Key-Based** | Multiple keys determine shard | Avoid hotspots, fine-grained control    | Complex routing                        | Multi-tenant systems                    |
| **Consistent Hashing**    | Keys on hash ring             | Minimal reshuffling, scalable           | Complex                                | Dynamic shard addition/removal, caching |
| **Geo / Location**        | Partition by region           | Low latency, compliance                 | Uneven load                            | Global apps, region-specific apps       |
| **Hybrid**                | Combine strategies            | Flexible, solves hotspots               | Very complex                           | Large-scale systems                     |