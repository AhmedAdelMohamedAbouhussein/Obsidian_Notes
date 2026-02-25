## 1️⃣ Definition

The **Bounded Knapsack Problem (BKP)** is a variant of the **0/1 Knapsack Problem** where each item has:

- Weight `w[i]`
    
- Value `v[i]`
    
- Maximum available **quantity** `num[i]` (bounded)
    

**Goal:** Maximize total value in a knapsack of capacity `W`, without exceeding the weight limit.

**Difference from 0/1 Knapsack:**

- In 0/1 Knapsack, you can take **at most one** of each item.
    
- In Bounded Knapsack, you can take **up to `num[i]`** copies of each item.
    

---

## 2️⃣ Problem Statement

Given:

- n items
    
- Arrays: `weight[]`, `value[]`, `count[]`
    
- Knapsack capacity `W`
![[{B45FCB3A-796E-48F0-82D9-23E9CC68C627}.png]]
## 3️⃣ Dynamic Programming Approach

We can solve BKP using **DP similar to 0/1 Knapsack** with an extra loop for bounded quantities.

### DP Array

- Let `dp[j]` = maximum value with knapsack capacity `j`
    

### Formula

For each item `i`:
![[{3BB51B0F-ABB5-4344-BEEF-AACFD97F0238}.png]]
## 4️⃣ Optimized DP — Binary Representation

To improve efficiency:

- **Split bounded item into powers of 2 copies**
    
- Transform Bounded Knapsack → **0/1 Knapsack problem**
    

Example:

- 5 copies → 1, 2, 2 (sum = 5)
    
- Reduces inner loop complexity from `O(num[i])` → `O(log num[i])`
    

---

## 5️⃣ Java Implementation (Simple Version)

![[{6384DE8F-6C11-405E-AFED-527B06644F60}.png]]

## 6️⃣ Time Complexity

- **Naive DP:** O(n * W * max(num[i]))
    
- **Optimized binary representation:** O(n * W * log(max(num[i])))
    

---

## 7️⃣ Space Complexity

- O(W) using **1D DP array** (rolling array optimization)
    
- Can also use O(n * W) for **2D DP table** if needed to reconstruct items
    

---

## 8️⃣ Differences With Other Knapsack Types

|Feature|0/1 Knapsack|Bounded Knapsack|Unbounded Knapsack|
|---|---|---|---|
|Copies per item|0 or 1|0..num[i]|Unlimited|
|Complexity (DP)|O(n*W)|O(n_W_num[i])|O(n*W)|
|Conversion to 0/1|Already 0/1|Use binary splitting|Not needed|