## 1️⃣ Definition

**Dijkstra’s algorithm** is a **graph algorithm** used to find the **shortest path** from a **single source** node to all other nodes in a **weighted graph**.

- Works only with **non-negative edge weights**
    
- Is a **greedy algorithm**
    

---

## 2️⃣ Core Idea

At each step:

1. Pick the **unvisited node with the smallest distance** from the source
    
2. Update distances to its neighbors if a shorter path is found
    
3. Mark the current node as visited
    
4. Repeat until all nodes are visited
    

---

## 3️⃣ Steps / Pseudocode

1. Initialize:
    
    - `dist[]` → distance from source to all nodes, initialize with ∞
        
    - `dist[source] = 0`
        
    - `visited[] = false` for all nodes
        
2. Repeat for all nodes:
    
    - Pick **node u** with minimum `dist[u]` that is not visited
        
    - Mark `u` as visited
        
    - For each neighbor `v` of `u`:
        
        - If `v` not visited and `dist[u] + weight(u,v) < dist[v]`:
            
            - Update `dist[v] = dist[u] + weight(u,v)`
                

---

## 4️⃣ Example

Graph:

       4  
  A -------- B  
  |    \        |  
  2     5     1  
  |         \   |  
  C  ------ D  
      3

Start from **A**:

1. dist[A]=0, dist[B]=∞, dist[C]=∞, dist[D]=∞
    
2. Pick **A**: neighbors B (4), C (2), D (5) → update distances
    
    - dist[B]=4, dist[C]=2, dist[D]=5
        
3. Pick **C** (dist=2): neighbor D → dist[D] = min(5, 2+3)=5
    
4. Pick **B** (dist=4): neighbor D → dist[D]=min(5, 4+1)=5
    
5. Pick **D** → done
    

Final distances from A:

A → A = 0  
A → B = 4  
A → C = 2  
A → D = 5

---

## 5️⃣ Java Implementation (Adjacency Matrix)
![[{633E4C5D-6689-4CB5-A40B-280DDA56EB5F}.png]]
## 6️⃣ Time Complexity

- **Using adjacency matrix:** O(V²)
    
- **Using adjacency list + min-heap (priority queue):** O(E log V)
    

Where:

- `V` = number of vertices
    
- `E` = number of edges
    

---

## 7️⃣ Space Complexity

- O(V²) for adjacency matrix
    
- O(V + E) for adjacency list
    

---

## 8️⃣ Properties

|Property|Explanation|
|---|---|
|Complete|✅ Finds path to all nodes|
|Optimal|✅ Finds **shortest paths** if all edge weights ≥ 0|
|Negative edges|❌ Not allowed (use Bellman-Ford instead)|
|Greedy|✅ Always chooses node with minimum distance next|

---

## 9️⃣ Comparison with A*

| Feature         | Dijkstra                            | A*                                |
| --------------- | ----------------------------------- | --------------------------------- |
| Heuristic       | ❌ None                              | ✅ Uses heuristic `h(n)`           |
| Path Optimality | ✅ Optimal                           | ✅ Optimal if heuristic admissible |
| Best use case   | All-pairs / single source           | Single start → goal               |
| Speed           | Slower on large graphs without goal | Faster with good heuristic        |