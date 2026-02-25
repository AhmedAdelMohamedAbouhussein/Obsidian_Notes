## 1️⃣ Definition

**Alpha-Beta Pruning** is an **optimization technique** for the **Minimax algorithm** used in **two-player games** like Chess, Tic-Tac-Toe, or Checkers.

- It **reduces the number of nodes evaluated** in the game tree
    
- Ensures the **same optimal move** as plain Minimax
    
- Speeds up decision-making for AI
    

---

## 2️⃣ Core Concept

In Minimax:

- **MAX player** tries to **maximize** the score
    
- **MIN player** tries to **minimize** the score
    

Alpha-Beta introduces two values:

|Parameter|Meaning|
|---|---|
|α (alpha)|Best value **so far for MAX** along the path to root|
|β (beta)|Best value **so far for MIN** along the path to root|

**Pruning Rule:**

- If at any point `α >= β`, stop evaluating that branch → **prune it**
    
- Because **no better outcome** can be obtained along this path
    

---

## 3️⃣ How It Works

1. Start at root (MAX node)
    
2. Traverse children recursively
    
3. Maintain `α` and `β` for MAX and MIN nodes
    
4. Update `α` or `β`:
    
    - MAX node: `α = max(α, value)`
        
    - MIN node: `β = min(β, value)`
        
5. If `α >= β` → prune remaining children
    

---

## 4️⃣ Example

Game tree (evaluation values at leaves):

          MAX  
       /      \  
     MIN       MIN  
    /  \      /  \  
    3    5    6    9

**Step-by-step:**

1. Start at left MIN node
    
    - Check left leaf = 3 → β = min(∞,3)=3
        
    - Check right leaf = 5 → β = min(3,5)=3
        
    - Left MIN returns 3 → MAX α = max(-∞,3)=3
        
2. Right MIN node:
    
    - Check left leaf = 6 → β = min(∞,6)=6
        
    - α=3 → α < β → continue
        
    - Check right leaf = 9 → β = min(6,9)=6
        
    - Right MIN returns 6 → MAX α = max(3,6)=6
        

No pruning in this small example, but in larger trees, many nodes are skipped.

---

## 5️⃣ Pseudocode

![[{01EC7864-81A0-4BCD-A838-CEC51FADCEF3}.png]]

6️⃣ Java Implementation (Simplified)
![[{CB640D72-89F7-427E-B1F1-4C6BA115A425}.png]]

## 7️⃣ Time Complexity

- **Without pruning (Minimax):** O(b^d)
    
    - b = branching factor, d = depth
        
- **With perfect alpha-beta pruning:** O(b^(d/2))
    
    - Roughly **double the depth you can search** in the same time
        

---

## 8️⃣ Space Complexity

- O(d) for recursive call stack
    
- Efficient, because we **do not store all nodes**
    

---

## 9️⃣ Properties

|Feature|Explanation|
|---|---|
|Optimality|✅ Finds same result as Minimax|
|Completeness|✅ Explores all necessary nodes|
|Speed|✅ Can prune many nodes → faster than Minimax|
|Requires ordering|⚠️ Better pruning if children are **sorted** in good order|

---

## 🔟 Key Tips

- Always pass **α = -∞, β = +∞** at root
    
- Sorting children **best moves first** increases pruning efficiency
    
- Commonly used in **Chess AI**, **Tic-Tac-Toe**, **Checkers**
    
- Pruning does **not affect correctness**, only efficiency