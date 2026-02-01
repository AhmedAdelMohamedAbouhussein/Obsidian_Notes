### Meaning

**Caching** is the process of **storing frequently accessed data in a fast storage layer** so that future requests can be served quickly, instead of repeatedly fetching from a slower source.

- Speeds up applications and reduces load on databases or servers.
    

---

## 1. How Caching Works

1. Client or system requests data.
    
2. Check **cache** first:
    
    - If data is present → **cache hit** → return immediately
        
    - If data is missing → **cache miss** → fetch from source, store in cache, then return
        
3. Cache can be **in-memory** (fast) or on **disk** (slower).
    

---

## 2. Types of Caching

|Type|Description|Example|
|---|---|---|
|**Browser Cache**|Stores web assets locally|CSS, JS, images|
|**Server Cache**|Stores responses/data at server|Redis, Memcached|
|**Database Cache**|Stores query results|Query caching in MySQL|
|**Application Cache**|Stores computed results|Memoization in code|

---

## 3. Benefits

- **Faster response times**
    
- **Reduced load** on backend servers or databases
    
- **Cost-efficient**: fewer expensive computations or database queries
    

---
## 4. Cache Strategies

- **LRU (Least Recently Used)**  
    Evicts the data that has **not been accessed for the longest time**.  
    Best when recently accessed data is likely to be reused.
    
- **LFU (Least Frequently Used)**  
    Evicts the data that has been **accessed the least number of times**.  
    Focuses on access frequency rather than time.
    
- **Write-through Cache**  
    Data is written to the **cache and the database at the same time**.  
    Provides strong consistency but results in **slower write performance**.
    
- **Write-back (Write-behind) Cache**  
    Data is written to the **cache first**, and the database is updated **later asynchronously**.  
    Improves write performance but risks **data loss** if the cache fails before syncing.
    
- **Write-around Cache**  
    Data is written **directly to the database**, bypassing the cache.  
    Prevents cache pollution from write-heavy or rarely-read data, but causes a **cache miss on first read**.
    
---

## 5. Memory Hook

- Think: **“Keep a fast copy of data you need often”**
    
- Cache = “shortcut storage”
    

---

## 6. One-Line Exam Answer

> Caching is storing frequently used data in a fast-access layer to improve performance and reduce load on slower sources.