### Meaning

**CAP Theorem** (Brewer’s Theorem) describes the **limitations of distributed systems**.

It states that a **distributed database** can only guarantee **two out of three properties at the same time**:

1. **C — Consistency**
2. **A — Availability**
3. **P — Partition Tolerance**

---

## 1. The Three Properties

### C — Consistency

- Every read receives the **most recent write**.
    
- All nodes return the same data at the same time.
    

### A — Availability

- Every request **receives a response**, even if it’s not the latest data.
    
- System never refuses requests.
    

### P — Partition Tolerance

- System continues to work **even if network partitions occur**.
    
- Network failures or node splits do not crash the system.
    

---

## 2. CAP Theorem Trade-offs

|Combination|Meaning|Example|
|---|---|---|
|CP|Consistent + Partition Tolerant|HBase, MongoDB (with strong consistency)|
|AP|Available + Partition Tolerant|Cassandra, DynamoDB|
|CA|Consistent + Available|Only possible if no network failures (rare in distributed systems)|

> Note: **Partition tolerance (P) is almost always needed** in distributed systems, so real-world systems usually choose **C or A** when partitions happen.

---

## 3. Memory Hook

- Think: **“Pick 2 out of 3: C, A, P”**
    
- Partition tolerance is almost mandatory in distributed systems → you must choose **Consistency OR Availability**.
    

---

## 4. One-Line Exam Answer

> The CAP Theorem states that in a distributed system, you can guarantee at most two of the three properties—Consistency, Availability, and Partition Tolerance—at the same time.