# **📌 Big-O Complexity for Common Data Structures**

| Data Structure               | Access                    | Search                    | Insertion                   | Deletion                    | Notes                                                   |
| ---------------------------- | ------------------------- | ------------------------- | --------------------------- | --------------------------- | ------------------------------------------------------- |
| **Array (static)**           | O(1)                      | O(n)                      | O(n)                        | O(n)                        | Insert/delete requires shifting elements                |
| **Dynamic Array**            | O(1)                      | O(n)                      | O(n)*                       | O(n)                        | *Amortized O(1) for append at end                       |
| **Singly Linked List**       | O(n)                      | O(n)                      | O(1) at head, O(n) at index | O(1) at head, O(n) at index | Cannot access arbitrary index quickly                   |
| **Doubly Linked List**       | O(n)                      | O(n)                      | O(1) at head/tail           | O(1) at head/tail           | Extra memory for prev pointer                           |
| **Stack (LIFO)**             | O(n)                      | O(n)                      | O(1)                        | O(1)                        | Only top accessible                                     |
| **Queue (FIFO)**             | O(n)                      | O(n)                      | O(1)                        | O(1)                        | Only front/back accessible                              |
| **Deque**                    | O(n)                      | O(n)                      | O(1) front/back             | O(1) front/back             | Double-ended queue                                      |
| **Hash Table**               | –                         | O(1) avg / O(n) worst     | O(1) avg / O(n) worst       | O(1) avg / O(n) worst       | Depends on hash collisions                              |
| **Hash Set / Hash Map**      | –                         | O(1) avg / O(n) worst     | O(1) avg / O(n) worst       | O(1) avg / O(n) worst       | HashMap = key-value                                     |
| **Binary Search Tree**       | O(log n) avg / O(n) worst | O(log n) avg / O(n) worst | O(log n) avg / O(n) worst   | O(log n) avg / O(n) worst   | Self-balancing trees (AVL, Red-Black) maintain O(log n) |
| **AVL Tree / Red-Black**     | O(log n)                  | O(log n)                  | O(log n)                    | O(log n)                    | Balanced BST                                            |
| **B-Tree**                   | O(log n)                  | O(log n)                  | O(log n)                    | O(log n)                    | Used in databases / disks                               |
| **Heap (Min/Max)**           | O(n)                      | O(n)                      | O(log n)                    | O(log n)                    | Binary heap                                             |
| **Trie / Prefix Tree**       | O(m)                      | O(m)                      | O(m)                        | O(m)                        | m = key length                                          |
| **Graph (Adjacency List)**   | O(V + E) traversal        | O(V + E)                  | O(1) edge insertion         | O(E) edge deletion          | V = vertices, E = edges                                 |
| **Graph (Adjacency Matrix)** | O(1) access               | O(V^2)                    | O(1) edge insertion         | O(1) edge deletion          | O(V^2) space                                            |
| **Circular Linked List**     | O(n)                      | O(n)                      | O(1) at head/tail           | O(1)                        | Similar to linked list, tail points to head             |
| **Skip List**                | O(log n) avg              | O(log n) avg              | O(log n) avg                | O(log n) avg                | Probabilistic balanced list                             |

