    Iterators in C++ are a powerful feature that allow you to traverse through elements of a container (like arrays, vectors, lists, etc.) without exposing the underlying structure of the container.
    They provide a uniform way to access elements in different types of containers.
    Iterators can be thought of as generalized pointers that can point to elements in a container.

    They support operations like incrementing, dereferencing, and comparison, which makes them versatile for iterating through collections.

    Iterators can be categorized into several types based on their capabilities:
    1. Input Iterators: Allow reading elements in a single pass (e.g., istream_iterator).
    2. Output Iterators: Allow writing elements in a single pass (e.g., ostream_iterator, back_inserter).
    3. Forward Iterators: Allow reading and writing elements in a single pass; can be incremented (e.g., forward_list).

    4. Bidirectional Iterators: Allow moving both forward and backward (e.g., list, set, multiset, map, multimap).
    5. Random Access Iterators: Allow jumping to any element in constant time (e.g., vector, deque, array).
    6. Contiguous Iterators: A refinement of random access iterators that guarantees elements are stored contiguously in memory (e.g., vector, array, string in C++17 and later).

  

    Examples of containers and their associated iterator types:
    - vector               -> Random Access, Contiguous Iterator
    - array                -> Random Access, Contiguous Iterator
    - deque                -> Random Access Iterator (not Contiguous!)
    - list (doubly linked) -> Bidirectional Iterator
    - forward_list         -> Forward Iterator
    - set                  -> Bidirectional Iterator
    - multiset             -> Bidirectional Iterator
    - map                  -> Bidirectional Iterator
    - multimap             -> Bidirectional Iterator
    - unordered_set        -> Forward Iterator
    - unordered_multiset   -> Forward Iterator
    - unordered_map        -> Forward Iterator
    - unordered_multimap   -> Forward Iterator
    - string               -> Random Access, Contiguous Iterator
    - istream_iterator     -> Input Iterator
    - ostream_iterator     -> Output Iterator
    - back_inserter (e.g., for vector) -> Output Iterator

  

    Adapters (no iterators exposed directly, controlled access only):
    - stack                -> Container Adapter (LIFO - Last In First Out)
    - queue                -> Container Adapter (FIFO - First In First Out)
    - priority_queue       -> Container Adapter (Heap-based, max-heap by default)

  
    Other Data Structures (typically used with custom traversal, not STL iterators):
    - Binary Tree / BST    -> Not part of STL; traversal via recursion or stack (preorder, inorder, etc.)
    - AVL Tree / Red-Black -> Implemented internally in std::map, std::set (self-balancing)
    - Graphs               -> Represented using adjacency list or matrix (no standard STL type, but often std::vector<vector<int>> or map/list)
    - Hash Table           -> unordered_* containers (use hash functions, Forward Iterator)
    - Heap                 -> std::priority_queue (max-heap), or make_heap/min_heap algorithms

  

    Summary:
    - Contiguous: vector, array, string
    - Random Access: vector, array, deque, string
    - Bidirectional: list, set, multiset, map, multimap
    - Forward: forward_list, unordered_set, unordered_map, unordered_multiset, unordered_multimap
    - Input/Output: stream iterators and adapters like back_inserter
    - No iterators (adapters): stack, queue, priority_queue
    - Custom traversal: trees, graphs, heaps (outside STL)

![[Pasted image 20250728164424.png]]