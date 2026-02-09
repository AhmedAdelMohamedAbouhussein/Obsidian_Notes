## 1. Definition

Dynamic Programming (DP) is an algorithmic technique used to solve problems by breaking them down into **smaller overlapping subproblems**, solving each subproblem **once**, and storing its result to avoid repeated computation.

Core idea: **store and reuse results** instead of recalculating them.

---

## 2. When to Use Dynamic Programming

A problem is suitable for DP if it satisfies **both** of the following properties:

### 2.1 Overlapping Subproblems

- The same subproblems are solved multiple times.
    
- Example: Fibonacci numbers, where `fib(n-1)` and `fib(n-2)` are recomputed repeatedly.
    

### 2.2 Optimal Substructure

- The optimal solution of a problem can be constructed from optimal solutions of its subproblems.
    
- Example: Shortest path problems, knapsack problems.
    

---

## 3. Why Dynamic Programming is Needed

### Naive Recursive Approach (Example: Fibonacci)

![[Pasted image 20260207205158.png]]

- Time Complexity: **O(2^n)**
    
- Problem: Massive recomputation
    

### Dynamic Programming Solution

- Each value is computed once
    
- Time Complexity reduced to **O(n)**
    

---

## 4. Two Main DP Approaches

### 4.1 Memoization (Top-Down DP)

- Uses recursion
    
- Stores results in an array or map
    
- Computes values only when needed
    

![[Pasted image 20260207205245.png]]

Characteristics:

- Recursive
    
- Easier to write
    
- Risk of stack overflow for large input
    

---

### 4.2 Tabulation (Bottom-Up DP)

- Uses iteration
    
- Solves smaller problems first
    
- Builds the solution step by step
    

![[Pasted image 20260207205306.png]]
Characteristics:

- Iterative
    
- No recursion overhead
    
- Usually preferred in interviews
    

---

## 5. DP State Representation

The **state** defines what the DP array represents.

Examples:

- `dp[i]` = result for first `i` elements
    
- `dp[i][j]` = result using first `i` items with capacity `j`
    
- `dp[i]` = maximum score until index `i`
    

Choosing the correct state is the most important step.

---

## 6. DP Transition (Recurrence Relation)

The transition defines **how to compute the current state from previous states**.

Example (Climbing Stairs):

dp[i] = dp[i - 1] + dp[i - 2]

This describes how solutions grow from smaller solutions.

---

## 7. Base Case

Base cases define the smallest subproblems that can be solved directly.

Examples:

- `dp[0] = 0`
    
- `dp[1] = 1`
    

Without correct base cases, DP will fail.

---

## 8. General Steps to Solve a DP Problem

1. Identify the **state**
    
2. Define the **transition (recurrence)**
    
3. Determine the **base cases**
    
4. Decide computation order (top-down or bottom-up)
    
5. Optimize space if possible
    

---

## 9. Common Types of Dynamic Programming Problems

### 9.1 1D DP

- Fibonacci
    
- Climbing Stairs
    
- House Robber
    
- Maximum Subarray
    

### 9.2 2D DP

- Knapsack
    
- Longest Common Subsequence (LCS)
    
- Edit Distance
    
- Matrix Path Problems
    

### 9.3 Grid DP

- Unique Paths
    
- Minimum Path Sum
    
- Number of ways to reach a cell
    

### 9.4 String DP

- Palindrome Partitioning
    
- Longest Palindromic Subsequence
    
- Edit Distance
    

---

## 10. DP vs Other Techniques

### DP vs Greedy

- Greedy makes locally optimal choices
    
- DP considers all possibilities and stores results
    
- Greedy is faster but not always correct
    

### DP vs Backtracking

- Backtracking explores all possibilities
    
- DP avoids repeated work by storing results
    

---

## 11. Space Optimization in DP

Often DP only depends on previous states.

Example:

dp[i] depends only on dp[i-1] and dp[i-2]

So we can replace the array with two variables.

---

## 12. Time and Space Complexity

- Time complexity usually equals the number of DP states
    
- Space complexity equals the size of the DP table
    

Optimizations may reduce space from O(n) to O(1).

---

## 13. Key Signals That a Problem Uses DP

- Asks for maximum or minimum
    
- Asks for number of ways
    
- Asks for optimal score or path
    
- Involves choices or decisions at each step
    

---

## 14. Common DP Mistakes

- Wrong state definition
    
- Missing base cases
    
- Wrong iteration order
    
- Using recursion without memoization
    

---

## 15. Summary

Dynamic Programming is a powerful technique used to efficiently solve complex problems by storing results of overlapping subproblems. Mastering DP requires practice in identifying states, transitions, and base cases.