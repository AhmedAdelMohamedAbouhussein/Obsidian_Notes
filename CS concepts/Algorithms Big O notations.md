# **1️⃣ Searching Algorithms**

| Algorithm      | Best Case | Average Case | Worst Case | Notes                          |
| -------------- | --------- | ------------ | ---------- | ------------------------------ |
| Linear Search  | O(1)      | O(n)         | O(n)       | Works on unsorted arrays       |
| Binary Search  | O(1)      | O(log n)     | O(log n)   | Requires **sorted array/list** |
| Ternary Search | O(1)      | O(log₃ n)    | O(log₃ n)  | Divide array into 3 parts      |

---

# **2️⃣ Sorting Algorithms**

|Algorithm|Best Case|Average Case|Worst Case|Notes|
|---|---|---|---|---|
|Bubble Sort|O(n)|O(n²)|O(n²)|Simple, rarely used|
|Selection Sort|O(n²)|O(n²)|O(n²)|Always O(n²)|
|Insertion Sort|O(n)|O(n²)|O(n²)|Efficient for nearly sorted arrays|
|Merge Sort|O(n log n)|O(n log n)|O(n log n)|Stable, recursive|
|Quick Sort|O(n log n)|O(n log n)|O(n²)|Divide & Conquer, in-place|
|Heap Sort|O(n log n)|O(n log n)|O(n log n)|Uses binary heap|
|Counting Sort|O(n+k)|O(n+k)|O(n+k)|k = max value, non-comparison sort|
|Radix Sort|O(nk)|O(nk)|O(nk)|k = digits/keys, stable|
|Bucket Sort|O(n+k)|O(n+k)|O(n²)|k = buckets, distributes elements|

---

# **3️⃣ Two Pointers / Sliding Window**

|Algorithm|Complexity|Notes|
|---|---|---|
|Two Pointers|O(n)|Often used for sorted arrays, pair sums, subarrays|
|Sliding Window (Fixed Window)|O(n)|Sum/average/max in subarrays|
|Sliding Window (Variable Window)|O(n)|Expand/shrink window dynamically|

---

# **4️⃣ Recursion / Divide & Conquer**

|Algorithm / Problem|Complexity|Notes|
|---|---|---|
|Factorial|O(n)|Linear recursion|
|Fibonacci (Naive Recursion)|O(2ⁿ)|Exponential|
|Fibonacci (Memoization/DP)|O(n)|Stores results|
|Merge Sort|O(n log n)|Divide & Conquer|
|Quick Sort|O(n log n) avg|Worst-case O(n²)|

---

# **5️⃣ Hashing / Hash Tables**

|Operation|Average|Worst-case|Notes|
|---|---|---|---|
|Insert / Delete / Search|O(1)|O(n)|Worst-case if hash collisions|
|Lookup in HashSet/HashMap|O(1)|O(n)|Java uses chaining or open addressing|

---

# **6️⃣ Graph Algorithms**

|Algorithm|Time Complexity|Notes|
|---|---|---|
|BFS / DFS|O(V + E)|V = vertices, E = edges|
|Dijkstra (Priority Queue)|O((V+E) log V)|Shortest path, non-negative weights|
|Bellman-Ford|O(V * E)|Handles negative weights|
|Floyd-Warshall|O(V³)|All-pairs shortest path|
|Prim (MST using PQ)|O((V+E) log V)|Minimum Spanning Tree|
|Kruskal (MST using union-find)|O(E log E)|Minimum Spanning Tree|

---

# **7️⃣ Dynamic Programming (DP)**

|Problem|Complexity|Notes|
|---|---|---|
|Fibonacci (DP)|O(n)|Memoization or tabulation|
|0/1 Knapsack|O(n*W)|n = items, W = capacity|
|Unbounded Knapsack|O(n*W)|Items can be chosen multiple times|
|Coin Change|O(n*amount)|Number of ways to make change|
|Longest Common Subsequence (LCS)|O(m*n)|m = length of string1, n = length of string2|
|Maximum Subarray (Kadane)|O(n)|Linear time for contiguous sum|

---

# **8️⃣ Greedy Algorithms**

|Algorithm|Complexity|Notes|
|---|---|---|
|Activity Selection|O(n log n)|Sort activities by finish time|
|Huffman Coding|O(n log n)|Priority queue for encoding|
|Minimum Spanning Tree (Prim/Kruskal)|O(E log V)|Greedy choice of edges|

---

# **9️⃣ Summary Table for Quick Revision**

|Category|Common Algorithms|Complexity Summary|
|---|---|---|
|Search|Linear, Binary|O(n), O(log n)|
|Sort|Bubble, Quick, Merge, Heap|O(n²) → O(n log n)|
|Two Pointers / Sliding Window|Subarray problems|O(n)|
|Recursion / Divide & Conquer|Factorial, Fibonacci, Merge Sort|O(n), O(2ⁿ), O(n log n)|
|Hashing|HashMap, HashSet|O(1) avg, O(n) worst|
|Graph|BFS, DFS, Dijkstra|O(V+E), O((V+E) log V)|
|DP|Knapsack, LCS, Fibonacci|O(n_W), O(m_n), O(n)|
|Greedy|Activity selection, MST|O(n log n), O(E log V)|