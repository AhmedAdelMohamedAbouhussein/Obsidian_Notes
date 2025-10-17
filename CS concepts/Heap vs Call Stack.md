## 🧠 **Heap vs Call Stack**

When a program runs, the computer needs memory to store variables, objects, and function calls.  
This memory is mainly divided into **two areas**:

- **Stack (Call Stack)** → for _function calls and local variables_
    
- **Heap** → for _dynamic memory allocation (objects, arrays, etc.)_
    

---

### 🧩 **1. Call Stack**

The **Call Stack** is a special region of memory that stores **function calls** and their **local variables**.

Every time a function is called:

- A **stack frame** (a small memory block) is created for that function.
    
- It contains:
    
    - The function’s **local variables**
        
    - The **return address** (where to go after the function finishes)
        
- When the function finishes, its frame is **popped off** the stack.
    

🧩 What happens in memory:

1. `main()` is called → a **stack frame** is created for it.
    
2. Inside `main()`, `add()` is called → a **new stack frame** is pushed for `add`.
    
3. When `add()` finishes → its frame is **popped** off the stack.
    
4. Execution goes back to `main()` → which then prints the result.
    

🧱 The stack is **LIFO (Last In, First Out)** — the last function called is the first to finish.

---

### ⚙️ **2. Heap**

The **Heap** is a large pool of memory used for **dynamic allocations** — data whose size or lifetime you don’t know in advance.

Objects, arrays, and data created using constructors or `new` (in C++, Java) or dynamically (in Python) live in the **heap**.

- The **heap** is managed manually (in C/C++) or automatically (with **garbage collection** in Java, Python, etc.)
    
- Variables in the heap remain there **until explicitly removed** or **garbage-collected**.


Here:

- `p1` (the reference) lives in the **stack**.
    
- The actual **Person object ("Ahmed")** lives in the **heap**.
    

When `p1` goes out of scope (no longer used), **Python’s garbage collector** frees the heap memory automatically.

---

### 🧮 **Comparison Table**

|Feature|**Call Stack**|**Heap**|
|---|---|---|
|**Purpose**|Store function calls and local variables|Store dynamically allocated objects and data|
|**Memory Management**|Automatic (push/pop)|Manual or automatic (depends on language)|
|**Access Speed**|Very fast|Slower|
|**Lifetime**|Until the function returns|Until explicitly freed or garbage-collected|
|**Structure**|Linear (LIFO)|Non-linear (tree-like, fragmented)|
|**Common Error**|Stack Overflow (too many nested calls)|Memory Leak (forgot to free memory)|