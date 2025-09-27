## 🔹 **Parallel Processing**

- **Definition:** Multiple tasks (or parts of a task) are executed **at the same time** using multiple processors/cores.
    
- **How it works:**
    
    - A job is divided into **independent subtasks**.
        
    - Each subtask runs on a separate core/processor simultaneously.
        
- **Example:**
    
    - Sorting a huge array by splitting it into chunks, sorting chunks in parallel, then merging.
        
    - GPUs running many threads at once for graphics.
        
- **Goal:** Minimize execution time by using more hardware resources.
    

---

## 🔹 **Pipelining**

- **Definition:** A single task is broken into **stages**, where each stage works on a different part of the input **in sequence**, like an assembly line.
    
- **How it works:**
    
    - While stage 1 is working on input A, stage 2 can simultaneously work on input B, stage 3 on input C, etc.
        
    - Tasks overlap, improving throughput.
        
- **Example:**
    
    - CPU instruction pipeline: Fetch → Decode → Execute → Write-back.
        
    - In a factory analogy: one worker cuts wood, another paints, another assembles — all at once on different pieces.
        
- **Goal:** Increase **throughput** (more results per unit time), not necessarily reduce latency of one task.

![[Pasted image 20250927174721.png]]

✅ **Think of it like this:**

- **Parallel** = many chefs each cooking a whole meal at once.
    
- **Pipeline** = one meal passes through multiple chefs, each specializing in a step (cutting, cooking, plating).