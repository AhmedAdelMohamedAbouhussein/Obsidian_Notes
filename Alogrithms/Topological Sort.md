## 1️⃣ Definition

**Topological Sort** is a **linear ordering of vertices in a Directed Acyclic Graph (DAG)** such that for every directed edge **u → v**, vertex **u** comes **before v** in the ordering.

- Only works on **DAGs** (Directed Acyclic Graphs)
    
- Useful in **scheduling, dependency resolution, and compiler design**
    

---

## 2️⃣ Use Cases

|Use Case|Description|
|---|---|
|Task scheduling|Ordering tasks based on dependencies|
|Build systems|Determine compilation order of source files|
|Course prerequisites|Determine order to take courses|
|Package managers|Resolve dependency graphs (APT, Yarn, PNPM)|
|Compiler|Instruction scheduling or AST processing|

---

## 3️⃣ Key Properties

1. Graph **must be directed**
    
2. Graph **must be acyclic**
    
3. Multiple valid topological sorts can exist
    
4. If the graph has a **cycle**, topological sort is **not possible**
    

---

## 4️⃣ Algorithms

### 4.1 Kahn’s Algorithm (BFS-based)

1. Compute **in-degree** of all vertices
    
2. Initialize queue with vertices having **in-degree 0**
    
3. While queue is not empty:
    
    - Remove a vertex `u`
        
    - Append `u` to the result list
        
    - For all neighbors `v` of `u`, decrement in-degree
        
    - If in-degree of `v` becomes 0, add it to the queue
        

**Time Complexity:** O(V + E)  
**Space Complexity:** O(V)

---

### 4.2 DFS-based Topological Sort

1. Initialize **visited array**
    
2. For each unvisited vertex, do **DFS**
    
3. After visiting all neighbors, **push vertex to stack**
    
4. Pop stack → gives **topological order**
    

**Time Complexity:** O(V + E)  
**Space Complexity:** O(V + E)

---

## 5️⃣ Example

Graph:

5 → 0 ← 4  
5 → 2 → 3  
2 → 3  
4 → 1

### Topological Sort Output (one possibility):

5, 4, 2, 1, 3, 0

---

## 6️⃣ Topological Sort in Java
![[{96E08EFC-3C1A-409E-A4F1-32FD3171EDC5}.png]]
## 7️⃣ Key Points / Tips

- DAG is mandatory; cycles → impossible
    
- Multiple valid topological orders exist
    
- BFS (Kahn) → easier to detect cycles
    
- DFS → uses stack and recursion
    
- Frequently used in **dependency resolution**, e.g., compiling source files, package managers