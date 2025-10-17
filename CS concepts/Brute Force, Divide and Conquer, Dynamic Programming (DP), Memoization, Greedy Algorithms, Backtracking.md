## 🧠 1. **Brute Force**

- **Idea:** Try **every possible solution** until you find the correct one.
- **Simple but slow** — no optimization.
- Works well only for **small inputs**.

#### 🔹 Example

- Checking all passwords to find the right one.
- Searching a number in an unsorted list by checking each element.

#### 🧩 Example Code (Python)
![[Pasted image 20251018012344.png]]
**Time Complexity:** O(n)

---

## ⚔️ 2. **Divide and Conquer**

- **Idea:** Break the problem into **smaller subproblems**, solve each one, and **combine** the results.
- Efficient for **sorted or structured data**.

#### 🔹 Steps

1. **Divide** the problem into smaller parts.
2. **Conquer** each part (recursively).
3. **Combine** the results.

#### 🧩 Example

- **Merge Sort**
- **Quick Sort**
- **Binary Search**

![[Pasted image 20251018012400.png]]
**Time Complexity:** O(log n)

---

## 💾 3. **Dynamic Programming (DP)**

- **Idea:** Solve complex problems by **breaking them into overlapping subproblems** and **reusing solutions**.
- Avoids recomputing results → saves time.

#### 🔹 Example

- Fibonacci sequence
- Shortest path (like in Dijkstra’s algorithm)
- Knapsack problem

#### 🧩 Example
![[Pasted image 20251018012423.png]]

**Time Complexity:** O(n)

---

## 🧠 4. **Memoization**

- A **technique used inside Dynamic Programming**.
- It **stores (caches)** results of expensive function calls so you don’t repeat work.
- Works well with **recursion**.

#### 🧩 Example
![[Pasted image 20251018012445.png]]

**Time Complexity:** O(n)

📝 **Memoization = Top-Down Dynamic Programming**

---

## 💰 5. **Greedy Algorithms**

- **Idea:** Make the **best (local) choice** at each step, hoping it leads to the best **global** solution.
- Works for problems where local choices = optimal overall solution.

#### 🔹 Example

- **Coin Change problem** (using largest coin first)
- **Dijkstra’s shortest path**
- **Kruskal’s / Prim’s algorithms** for minimum spanning trees

#### 🧩 Example
![[Pasted image 20251018012506.png]]

## 🔄 6. **Backtracking**

- **Idea:** Try a possible solution; if it doesn’t work, **go back (backtrack)** and try another.
- Used in **search and constraint problems**.

#### 🔹 Example

- Sudoku Solver
- N-Queens Problem
- Maze Solving

#### 🧩 Example
![[Pasted image 20251018012522.png]]

**Time Complexity:** Often exponential (O(2ⁿ))

---

## ⚙️ Summary Table

|Technique|Main Idea|Example Problems|Efficiency|
|---|---|---|---|
|**Brute Force**|Try all possibilities|Linear search, password cracking|❌ Slow|
|**Divide & Conquer**|Split, solve, and combine|Merge sort, binary search|⚡ Fast|
|**Dynamic Programming**|Store and reuse overlapping results|Fibonacci, Knapsack|✅ Efficient|
|**Memoization**|Cache results (top-down DP)|Recursive Fibonacci|✅ Efficient|
|**Greedy**|Pick best local choice|Dijkstra, Huffman coding|⚡ Fast if applicable|
|**Backtracking**|Explore all paths, backtrack if fail|Sudoku, N-Queens|❌ Slow but complete|

---

### 💡 Simple Analogy

|Approach|Analogy|
|---|---|
|**Brute Force**|Try every door until one opens|
|**Divide & Conquer**|Split the house into sections and search each|
|**Dynamic Programming**|Remember which rooms you already searched|
|**Memoization**|Write down the results so you don’t recheck|
|**Greedy**|Always open the closest unlocked door|
|**Backtracking**|Try one door; if it’s locked, go back and try another|
