### Definition

**Denormalization** is the process of **adding redundant data or combining tables** in a database to **improve read/query performance**, at the cost of some storage space and write complexity.

> In short: **“Store some data twice to make reads faster.”**

---

### Why Denormalize?

- Reduce the number of **joins** in queries
    
- Improve **read performance**
    
- Support **reporting and analytics** where speed matters more than strict normalization
    

---

### How It Works

1. **Combine tables**
    
    - Example: Store `customer_name` directly in `orders` table instead of joining with `customers` table.
        
2. **Duplicate columns**
    
    - Store calculated fields (like `total_price`) to avoid computing on the fly.
        
3. **Pre-aggregate data**
    
    - Example: Store `monthly_sales` instead of summing each order every time.
        

---

### Advantages ✅

- Faster **read queries**
    
- Simplifies queries (fewer joins)
    
- Reduces database load for **read-heavy workloads**
    

---

### Disadvantages ❌

- **Redundant data** → more storage needed
    
- Risk of **data inconsistency**
    
- Slower **writes/updates** (need to update multiple places)
    
- Harder to maintain **referential integrity**
    

---

### Use Cases

- Data warehouses / OLAP systems
    
- Reporting and analytics
    
- Read-heavy applications (e.g., dashboards, recommendation engines)
    
- Caching computed results
    

---

### Example

**Normalized Tables**
![[Pasted image 20260201214238.png]]
Denormalized Table
![[Pasted image 20260201214252.png]]
- **Benefit:** No need to join `Orders` with `Customers` to get the customer name.
    

---

### One-line exam definition ✅

> **Denormalization is the deliberate introduction of redundancy in a database to improve read performance.**