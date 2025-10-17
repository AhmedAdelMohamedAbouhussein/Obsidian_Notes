## 🧠 **What Are Threads?**

A **thread** is the **smallest unit of execution** within a program.  
You can think of a **thread** as a _mini program_ running inside your main program.

Every program starts with **one main thread**, but it can create **multiple threads** to do different tasks _at the same time_ (or appear to).

---

### ⚙️ **Example Idea**

Imagine you’re writing a music player app:

- 🎵 One thread plays the song.
    
- 🖼️ Another thread updates the visuals.
    
- 📡 Another thread downloads the next track.
    

All of these happen _together_ — without waiting for one another.

---

## 🧩 **1. Process vs Thread**

|Feature|**Process**|**Thread**|
|---|---|---|
|**Definition**|A complete, independent program|A lightweight part of a process|
|**Memory**|Has its own memory space|Shares memory with other threads in the same process|
|**Communication**|Needs inter-process communication (IPC)|Easier — since they share memory|
|**Creation cost**|High|Low|
|**Failure**|One process crash doesn’t affect others|If one thread crashes, it can affect the whole process|

---

### 💡 Example in Python
![[Pasted image 20251018014055.png]]
🧩 **What happens:**

- `t1` and `t2` run **at the same time**.
    
- You’ll see **numbers and letters** printed **interleaved** — not in strict order.
    

---

## 🧮 **2. Thread Lifecycle**

A thread goes through these main states:

1. **New** → created but not started.
    
2. **Runnable** → ready to run.
    
3. **Running** → executing code.
    
4. **Blocked / Waiting** → waiting for some event (e.g., I/O).
    
5. **Terminated** → finished executing.
    

---

## 🔐 **3. Shared Memory & Synchronization**

Because threads **share the same memory**, problems can occur if two threads try to change the same data at once.  
This is called a **race condition**.

🧩 **Example problem:**

count = 0  
def increment():     
	global count    
	for _ in range(1000000):        
		count += 1`

If two threads run `increment()` at the same time, the final result **may not be 2,000,000** because both access `count` simultaneously.

💡 To fix that, we use **locks**:

`lock = threading.Lock() def increment():     global count     for _ in range(1000000):         with lock:             count += 1`

The **lock** makes sure only one thread modifies the variable at a time.

---

## ⚡ **4. Advantages of Threads**

✅ Faster context switching (compared to processes)  
✅ Better performance on I/O tasks (like file or network)  
✅ Easier data sharing (same memory)  
✅ Keeps apps responsive (e.g., GUI doesn’t freeze)

---

## ⚠️ **5. Disadvantages**

❌ Harder to debug (race conditions, deadlocks)  
❌ CPU-bound tasks don’t always get faster in Python (because of the **GIL**)  
❌ Crashing one thread can affect the whole process

---

## 🧭 **In Short**

|Concept|Meaning|
|---|---|
|**Thread**|Smallest unit of program execution|
|**Main Thread**|The default thread where your program starts|
|**Multithreading**|Running multiple threads at once|
|**Lock**|Prevents two threads from accessing shared data at the same time|

---

### 💡 Analogy

🧑‍🍳 Think of a restaurant:

- The **process** is the whole restaurant (kitchen, waiters, etc.)
    
- Each **thread** is a chef working on one dish.
    
- They share the same kitchen (memory).
    
- If two chefs try to use the same stove (variable) → chaos happens (race condition)! 😅