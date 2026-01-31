### Meaning

**Sharding** is a **database scaling technique** where a large database is **split into smaller, faster, more manageable pieces called shards**.

- Each shard holds **part of the data**.
    
- All shards together represent the **complete database**.
    

---

## 1. How Sharding Works

- **Horizontal Sharding (most common):**
    
    - Each shard contains **rows of a table**.
        
    - Example: Users with `userID 1-1000` → Shard 1, `1001-2000` → Shard 2.
        
- **Vertical Sharding:**
    
    - Each shard contains **columns of a table**.
        
    - Example: One shard for user profile info, another for login info.
        
- **Key-Based Sharding:**
    
    - A **shard key** determines which shard a record goes to.
        
    - Example: `userID % numberOfShards`
        

---

## 2. Why Sharding is Used

- Improve **performance**: smaller datasets per shard → faster queries
    
- Improve **scalability**: easy to add more shards as data grows
    
- Reduce **load on a single database**
    
- Enables **distributed storage**
    

---

## 3. Trade-offs

- Complexity: queries across shards can be harder
    
- Data consistency: harder to maintain ACID across shards
    
- Rebalancing shards can be tricky
    

---

## 4. Examples

- Large websites like:
    
    - Twitter → shards tweets by user ID
        
    - Facebook → shards user data by region
        
    - MongoDB, Cassandra → built-in sharding support
        

---

## 5. Memory Hook

- Think: **“Split a big database into smaller pieces to make it faster and scalable”**
    
- “Shards = slices of the database”
    

---

## 6. One-Line Exam Answer

> Sharding is a technique for splitting a large database into smaller pieces called shards, each holding a subset of data, to improve performance and scalability.