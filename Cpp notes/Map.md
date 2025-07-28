    A map is a collaction of key-value pairs: k -> v
    order by insertion: elements are sorted in the order they are inserted
    order by sorting: elements are sorted in ascending order by default

    In cpp similar a set
        A map is in sorted order.
        An unordered map is not ordered by insertion, nor sorted.


  
// ================================================
// std::map vs std::unordered_map in C++
// ================================================

  

// std::map:
// - Implemented as a Red-Black Tree (a self-balancing binary search tree).
// - Stores key-value pairs in sorted (ascending) order by key.
// - All operations (insert, find, erase, etc.) take O(log n) time.
// - Worst-case time complexity: O(log n).

// std::unordered_map:
// - Implemented as a Hash Table.
// - Stores key-value pairs with no particular order (unordered).
// - Average-case time complexity for insert, find, erase: O(1).
// - Worst-case time complexity: O(n) in case of hash collisions.
// - Requires good hash function and sufficient space to minimize collisions.

  
// Summary:
// - Use std::map when you need ordered keys or in-order traversal.
// - Use std::unordered_map when you need faster average performance and don't care about order.

![[Pasted image 20250728164615.png]]
![[Pasted image 20250728164631.png]]