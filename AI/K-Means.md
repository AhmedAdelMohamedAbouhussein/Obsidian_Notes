# **1️⃣ What is K-Means?**

**K-Means** is an **unsupervised machine learning algorithm** used to **group (cluster) similar data points**.

- “K” = number of clusters you want to find.
    
- The algorithm assigns each data point to the **closest cluster** based on feature similarity.
    

---

# **2️⃣ How it works (step by step)**

Suppose you have N data points (e.g., 512-dim vectors from your images):

1. **Choose K random points as initial cluster centers** (called **centroids**).
    
2. **Assign each point to the nearest centroid** (using distance like Euclidean distance).
    
3. **Recompute the centroids** by taking the **average of all points in that cluster**.
    
4. **Repeat steps 2–3** until:
    
    - Assignments stop changing, or
        
    - Maximum number of iterations is reached

---

# **3️⃣ Visual Example (2D for simplicity)**

Imagine 10 points on a plane and K=2:
![[Pasted image 20251201015436.png]]
- Step 1: Randomly pick 2 points as centroids 🔴🔵
- Step 2: Assign points to closest centroid
- Step 3: Move centroids to average of points    
- Repeat → clusters stabilize

# **4️⃣ Key Points**

- **Unsupervised** → no labels needed, it finds structure in the data automatically.
- **Distance metric** → usually Euclidean distance.
- **Output** →
    - Cluster labels for each point
    - Cluster centroids (mean vectors)