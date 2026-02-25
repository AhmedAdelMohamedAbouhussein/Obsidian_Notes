## 1️⃣ Definition

**A*** is a **graph/tree search algorithm** used to find the **shortest path** from a start node to a goal node.

- It is **informed** (uses heuristics)
    
- Combines benefits of:
    
    - **Dijkstra’s algorithm** (guaranteed shortest path)
        
    - **Greedy Best-First Search** (uses heuristics to guide search)
        

---

## 2️⃣ Key Concept

A* uses a **cost function**:

f(n)=g(n)+h(n)f(n) = g(n) + h(n)f(n)=g(n)+h(n)

Where:

- `f(n)` → total estimated cost of the cheapest path through node `n`
    
- `g(n)` → cost from **start** to node `n` (known)
    
- `h(n)` → **heuristic estimate** from node `n` to **goal** (unknown, guessed)
    

The algorithm **expands nodes with the lowest `f(n)` first**.

---

## 3️⃣ Heuristic Function `h(n)`

The heuristic is critical:

- Must be **admissible** (never overestimates cost to goal) → ensures **optimality**
    
- Must be **consistent** (monotonic) → ensures efficiency
    

Common heuristics:

|Type|Formula|Use Case|
|---|---|---|
|Manhattan distance|`|x1-x2|
|Euclidean distance|`sqrt((x1-x2)^2 + (y1-y2)^2)`|Grid with diagonal movement|
|Chebyshev distance|`max(|x1-x2|

---

## 4️⃣ Algorithm Steps

**Input:** start node `S`, goal node `G`

1. Initialize:
    
    - `openSet` → nodes to explore (priority queue by `f(n)`)
        
    - `closedSet` → nodes already explored
        
    - `gScore[start] = 0`
        
    - `fScore[start] = h(start)`
        
2. While `openSet` is not empty:
    
    - Pick node `current` with lowest `f(current)`
        
    - If `current == goal`, reconstruct path and return
        
    - Move `current` to `closedSet`
        
    - For each neighbor `n` of `current`:
        
        - Skip if in `closedSet`
            
        - `tentative_g = g(current) + cost(current, n)`
            
        - If `n` not in `openSet` or `tentative_g < g(n)`:
            
            - `cameFrom[n] = current`
                
            - `g(n) = tentative_g`
                
            - `f(n) = g(n) + h(n)`
                
            - Add `n` to `openSet` if not already
                
3. If `openSet` is empty → no path exists
    

---

## 5️⃣ Example (Grid)

Consider a 5x5 grid (0 = free, 1 = obstacle):

S 0 1 0 G  
0 0 1 0 0  
0 0 0 0 0

- `S` → start
    
- `G` → goal
    

Use **Manhattan distance** as heuristic:

- `f(n) = g(n) + h(n)`
    
- Expand nodes with **lowest `f(n)`** first
    

A* will find the **shortest path** while avoiding obstacles efficiently.

---

## 6️⃣ Java Implementation (Simplified)

![[{D36B3E52-9074-4C1F-B925-CF7D80711B90}.png]]
![[{B4678E32-AA95-46E0-B098-947706F8D5FC}.png]]
