## 1️⃣ Definition

**Bucket Sort** is a **distribution-based sorting algorithm** that:

1. Divides elements into multiple buckets
    
2. Sorts each bucket individually
    
3. Merges all buckets to form the final sorted array
    

It works best when:

- Data is **uniformly distributed**
    
- The range of values is known
    
- Often used for **floating-point numbers**
    

---

# 2️⃣ Core Idea

Instead of repeatedly comparing elements (like QuickSort or MergeSort), we:

- Distribute elements into logical groups (buckets)
    
- Sort each group separately
    
- Concatenate results
    

This reduces heavy comparisons when distribution is good.

---

# 3️⃣ Algorithm Steps

Given array `arr` of size `n`:

1. Create `n` empty buckets
    
2. Distribute elements into buckets
    
3. Sort each bucket
    
4. Merge all buckets
    

---

# 4️⃣ Example (Floating Numbers 0–1)

Input:

[0.78, 0.17, 0.39, 0.26, 0.72, 0.94, 0.21, 0.12, 0.23, 0.68]

Bucket index formula:

index = (int)(n * value)

Example:

0.78 → (int)(10 × 0.78) = 7  
0.17 → 1

After distribution:

Bucket[1]: 0.17, 0.12  
Bucket[2]: 0.26, 0.21, 0.23  
Bucket[7]: 0.78, 0.72  
...

Sort each bucket → Merge → Final sorted array.

---

# 5️⃣ Java Implementation (Using ArrayList)

Java does not allow dynamic array-of-arrays easily, so we use `ArrayList`.
![[Pasted image 20260225220203.png]]

# 6️⃣ Time Complexity

Let:

- `n` = number of elements
    
- `k` = number of buckets
    

### Best Case (Uniform Distribution)

Each bucket contains very few elements:

O(n)

### Average Case

O(n + k)

If k ≈ n → O(n)

### Worst Case

If all elements go into one bucket:

O(n²)

Because sorting one large bucket takes quadratic time.

---

# 7️⃣ Space Complexity

O(n + k)

Requires extra memory for buckets.

Not in-place.

---

# 8️⃣ Stability

✅ Stable (if internal sort is stable)

`Collections.sort()` uses **TimSort**, which is stable.

---

# 9️⃣ When to Use Bucket Sort

Good for:

- Uniformly distributed floating numbers
    
- Large datasets with known range
    
- When linear time is achievable
    

Not good for:

- Highly skewed data
    
- Unknown distribution
    
- Small arrays (overhead is unnecessary)

# 1️⃣1️⃣ Difference from Counting Sort

|Feature|Bucket Sort|Counting Sort|
|---|---|---|
|Works with floats|✅|❌|
|Needs uniform distribution|✅|❌|
|Uses buckets of lists|✅|❌|
|Uses frequency array|❌|✅|

---

# 1️⃣2️⃣ Key Insight

Bucket Sort becomes fast because:

If data is evenly spread →  
Each bucket is small →  
Sorting small buckets is cheap →  
Total cost becomes linear.

The **distribution assumption** is the most important concept.