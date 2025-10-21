## 1. **Definition**

A **thread** is the **smallest unit of execution** within a process.  
Thread architecture defines **how hardware organizes, schedules, and executes threads** on the processor.

🧠 In simple terms:

> A **thread** = a mini-program that runs independently, sharing resources with others.

---

## 2. **Threads in CPUs vs GPUs**

|Feature|CPU Threads|GPU Threads|
|---|---|---|
|Count|Few (2–32 threads typically)|Thousands (10,000+ concurrently)|
|Focus|Task parallelism|Data parallelism|
|Scheduling|Complex OS-managed|Lightweight hardware-managed|
|Latency|Low|High (hidden by massive concurrency)|
|Control|Each thread executes unique instructions|Groups of threads execute same instructions (SIMT)|

---

## 3. 🧩 **CPU Thread Architecture**

### **Structure**

- Each CPU core can handle **1–2 threads** (with **Hyper-Threading** / **SMT**).
    
- Threads **share core resources** (ALU, cache, registers).
    
- OS **scheduler** decides which thread runs on which core.
    

### **Execution Model**

- Designed for **low-latency, high-control** workloads (like logic, branching, I/O).
    
- Threads often perform **different tasks**.
    

### **Diagram (Simplified)**
![[Pasted image 20251021222303.png]]

## 4. ⚡ **GPU Thread Architecture**

GPUs are designed for **massive parallelism** — executing thousands of lightweight threads simultaneously.

### **Hierarchical Organization**

Threads are organized in multiple levels:

| Level                        | Description                                                        | Example (CUDA)     |
| ---------------------------- | ------------------------------------------------------------------ | ------------------ |
| **Thread**                   | Single execution unit                                              | `threadIdx.x`      |
| **Warp/Wavefront**           | Group of 32 threads (NVIDIA) or 64 (AMD) executing together        | 32 threads         |
| **Thread Block / Workgroup** | Collection of warps executing on one Streaming Multiprocessor (SM) | 256–1024 threads   |
| **Grid**                     | All blocks launched by one kernel                                  | Whole GPU workload |

---

### **Visualization**
![[Pasted image 20251021222317.png]]

Each **thread** executes the same **kernel function**, but operates on **different data** (SIMT model).

---

## 5. **Streaming Multiprocessor (SM) / Compute Unit (CU)**

Each GPU contains multiple **SMs (NVIDIA)** or **CUs (AMD)** — the main hardware blocks that execute threads.

### Inside Each SM:

- Multiple **CUDA Cores / ALUs**
    
- **Warp Scheduler** (decides which warps execute)
    
- **Register file** (for active threads)
    
- **Shared memory / L1 cache**
    
- **Tensor cores** (in modern GPUs for AI workloads)
    

### Example:

> An NVIDIA RTX 4090 has **128 SMs**,  
> each handling **64 warps × 32 threads = 2048 active threads per SM**  
> → Over **250,000 concurrent threads** across the GPU!

---

## 6. 🧮 **GPU Thread Execution Flow**

1. The **CPU launches a kernel** with a grid of threads.
    
2. GPU **allocates thread blocks** to SMs.
    
3. Each SM divides blocks into **warps**.
    
4. The **warp scheduler** issues instructions to active threads.
    
5. If some threads diverge (branch differently), the warp executes each path serially — this is **warp divergence**.
    

---

## 7. **Memory Access Model**

|Memory Type|Scope|Used By|
|---|---|---|
|**Registers**|Per thread|Local variables|
|**Shared Memory**|Per block|Fast data sharing within a block|
|**Global Memory (VRAM)**|All threads|Large but slow|
|**Constant/Texture Memory**|Read-only|Optimized for specific access patterns|

---

## 8. **Thread Scheduling and Latency Hiding**

- GPU hides latency not by speeding up threads, but by **switching between warps** instantly.
    
- While one warp waits for memory → another warp runs.
    
- No OS context switching — it’s handled in **hardware**.
    

> ⚡ This is why GPUs excel in workloads with **many simple operations** (AI, rendering, physics).

---

## 9. **Thread Synchronization**

- Threads within a **block** can synchronize using:
    
    `__syncthreads();`
    
- Threads across **blocks** cannot directly sync — they communicate through **global memory**.
    

---

## 10. **Comparison Summary**

|Feature|CPU|GPU|
|---|---|---|
|Thread Count|Few (2–32)|Thousands|
|Thread Weight|Heavy (OS-managed)|Light (hardware-managed)|
|Scheduling|Complex, slow|Simple, fast|
|Execution Model|MIMD (Multiple Instruction, Multiple Data)|SIMT (Single Instruction, Multiple Threads)|
|Latency Handling|Out-of-order execution|Warp scheduling|
|Use Case|Sequential, logic-heavy tasks|Parallel, data-heavy tasks|

---

## 11. **Analogy**

> - A **CPU** is like a few expert chefs who can cook any meal with precision (threads = chefs).
>     
> - A **GPU** is like a massive kitchen with hundreds of cooks each making one simple dish at once.
>     

---

✅ **In summary:**

- **CPU threads** = few, powerful, independent.
    
- **GPU threads** = many, lightweight, cooperative.
    
- Together, they deliver **heterogeneous computing power** — CPU manages control, GPU handles parallel workloads.