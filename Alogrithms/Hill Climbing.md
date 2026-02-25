## 1️⃣ Definition

**Hill Climbing** is a **local search algorithm** used in **optimization problems**.

- Starts with an initial solution
    
- Iteratively moves to a **neighbor solution** with **higher value** (or lower cost, if minimizing)
    
- Stops when no neighbor is better → **local maximum** (or minimum)
    

It’s called “Hill Climbing” because it’s like **climbing uphill to reach the peak**.

---

## 2️⃣ Key Concept

- Problem space = **search space**
    
- Each solution has a **value (fitness / cost)**
    
- Algorithm **greedily** chooses the **best neighbor**
    
- Does **not backtrack**
    

---

## 3️⃣ Types of Hill Climbing

1. **Simple Hill Climbing**
    
    - Evaluates **one neighbor at a time**
        
    - Moves to neighbor if **better**
        
    - Stops if no improvement
        
2. **Steepest-Ascent Hill Climbing**
    
    - Evaluates **all neighbors**
        
    - Moves to **best among neighbors**
        
3. **Stochastic Hill Climbing**
    
    - Chooses randomly among **better neighbors**
        
    - Avoids deterministic traps
        
4. **Random-Restart Hill Climbing**
    
    - Runs Hill Climbing **multiple times** with **different initial states**
        
    - Increases chance of finding **global optimum**
        

---

## 4️⃣ Algorithm Steps (Simple Hill Climbing)

1. Start with **initial solution** `current`
    
2. Loop:
    
    - Find **neighbor(s)** of `current`
        
    - Select **neighbor with highest value**
        
    - If neighbor better than `current` → move to neighbor
        
    - Else → **stop** (local maximum reached)
        
3. Return `current` as the solution
    

---

## 5️⃣ Example (Maximization)

Maximize `f(x) = - (x-3)^2 + 9` over x ∈ [0, 6]

1. Start at x = 0 → f(0) = 0
    
2. Evaluate neighbors: x = 0.1 → f(0.1) = 0.99
    
3. Move to x = 0.1 → continue moving right
    
4. Eventually reach x = 3 → f(3) = 9 → **local/global maximum**
    

---

## 6️⃣ Java Implementation (Simple Hill Climbing)

![[{EB29551A-362D-436D-A122-448AADFF6330}.png]]

## 7️⃣ Time Complexity

- Depends on **number of steps** and **neighbors** evaluated
    
- **Simple Hill Climbing:** O(n) for n iterations
    
- **Steepest-Ascent:** O(n × k), k = number of neighbors
    

---

## 8️⃣ Space Complexity

- O(1) for simple hill climbing (only need current value)
    
- O(k) if storing neighbors
    

---

## 9️⃣ Advantages

- Simple to implement
    
- Efficient for **problems with smooth search space**
    
- Can find **good local solutions quickly**
    

---

## 🔟 Disadvantages / Limitations

1. **Local Maximum / Minimum**
    
    - May stop at suboptimal peak
        
2. **Plateau / Flat Area**
    
    - No neighbor is better → stuck
        
3. **Ridges / Narrow Peaks**
    
    - May miss global optimum
        
4. **No Backtracking**
    
    - Greedy → not guaranteed to find global optimum
        

---

## 1️⃣1️⃣ Improvements

- **Random-Restart:** Start from multiple points
    
- **Stochastic Hill Climbing:** Random selection among better neighbors
    
- **Simulated Annealing:** Accept worse solutions occasionally to escape local maxima