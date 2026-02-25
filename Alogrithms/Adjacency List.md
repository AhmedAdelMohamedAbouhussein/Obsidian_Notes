An **adjacency list** is a **graph representation** where:

- Each **vertex** stores a **list of its adjacent vertices**
    
- Efficient for **sparse graphs** (few edges)
    

Compared to an **adjacency matrix**:

|Feature|Adjacency List|Adjacency Matrix|
|---|---|---|
|Space Complexity|O(V + E)|O(V²)|
|Best for|Sparse graphs|Dense graphs|
|Checking edge existence|O(degree)|O(1)|
|Iterating neighbors|O(degree)|O(V)|

Where:

- `V` = number of vertices
    
- `E` = number of edges
    

---

## 2️⃣ Structure

For a graph `G = (V, E)`:

- Maintain an **array or list of size V**
    
- Each element points to a **linked list or dynamic array** of neighbors
    

Example:

Graph:

0 → 1, 2  
1 → 2  
2 → 0, 3  
3 → 3

Adjacency List:

0: 1 → 2  
1: 2  
2: 0 → 3  
3: 3

---

## 3️⃣ Advantages

- Space-efficient for **sparse graphs**
    
- Iterating neighbors is fast (O(degree))
    
- Can easily store **weighted edges**
    

---

## 4️⃣ Disadvantages

- Checking if an edge exists between two vertices is slower: O(degree of vertex)
    
- Not as simple as a matrix for **dense graphs**
    

---

## 5️⃣ Java Implementation
![[{37455E80-95FB-42D8-9770-6F126FEBC57D}.png]]
Output:

0: 1 2  
1: 2  
2: 0 3  
3: 3

## 6️⃣ Space Complexity

- **O(V + E)**
    
    - V → array of lists
        
    - E → total number of edges in all lists
        

---

## 7️⃣ Time Complexity

|Operation|Complexity|
|---|---|
|Iterate all neighbors of v|O(degree(v))|
|Check if (u,v) edge exists|O(degree(u))|
|Add an edge|O(1) (linked list)|

---

## 8️⃣ Weighted Graph Variant

- Store **pairs** `(neighbor, weight)` instead of just `neighbor`
    
- Example using `class Edge` or `Map<Integer, Integer>`

![[{C7FA82D2-3BB1-4EB7-9814-89EACE1C2217}.png]]
## 9️⃣ Key Points for Exams

- Use **adjacency list** for **sparse graphs**
    
- **Space-efficient** (O(V+E)) vs adjacency matrix (O(V²))
    
- Can easily support **directed/undirected**, **weighted/unweighted** graphs
    
- Used in **DFS, BFS, Dijkstra, Prim, Kruskal** algorithms