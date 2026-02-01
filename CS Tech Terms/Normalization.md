### Definition

**Normalization** is the process of **organizing a database to reduce redundancy and dependency**, by dividing tables into smaller, related tables.

> In short: **“Eliminate duplicate data and enforce relationships.”**

---

### Goals of Normalization

1. Remove **redundant data** (avoid storing the same info in multiple places)
    
2. Ensure **data integrity** (consistent data across the database)
    
3. Simplify **updates, inserts, and deletes**
    
4. Avoid **anomalies**:
    
    - **Update anomaly** – changing data in one place but not others
        
    - **Insertion anomaly** – can’t insert without other data
        
    - **Deletion anomaly** – deleting a row removes unintended data
        

---

### Normal Forms (Common)

|Normal Form|Rule / Goal|
|---|---|
|**1NF (First Normal Form)**|Each column has **atomic values**, no repeating groups|
|**2NF (Second Normal Form)**|**1NF + all non-key columns fully depend on the primary key** (no partial dependency)|
|**3NF (Third Normal Form)**|**2NF + no transitive dependency** (non-key columns depend only on primary key)|
|**BCNF (Boyce-Codd NF)**|Stronger version of 3NF; **every determinant is a candidate key**|
|**4NF**|No multi-valued dependencies|
|**5NF**|No join dependencies beyond candidate keys|

---

### Advantages ✅

- Eliminates **redundancy**
    
- Improves **data consistency**
    
- Reduces **storage usage**
    
- Makes **maintenance easier**
    

---

### Disadvantages ❌

- May require **more joins**, which can **slow read queries**
    
- Complex **queries for reporting or analytics**
    
- Can **over-normalize** for read-heavy systems
    

---

### Example

**Unnormalized Table**
![[Pasted image 20260201214356.png]]
Normalized Tables
![[Pasted image 20260201214406.png]]
- Eliminates duplicate customer data
    
- Easier to update customer info
    

---

### One-line exam definition ✅

> **Normalization is the process of structuring a database to minimize redundancy and maintain data integrity.**
> 