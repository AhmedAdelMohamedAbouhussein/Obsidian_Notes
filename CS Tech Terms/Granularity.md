## 1️⃣ Definition

**Granularity** refers to the **level of detail or size of the smallest unit** in a system, process, or dataset.

- Fine-grained → smaller, more detailed units
    
- Coarse-grained → larger, less detailed units
    

It’s a general concept used in **computer science, parallel computing, databases, and software design**.

---

## 2️⃣ Granularity in Different Contexts

### 2.1 Parallel Computing

- **Task granularity**: Size of tasks divided among processors
    
    - **Fine-grained**: many small tasks, more communication overhead
        
    - **Coarse-grained**: fewer large tasks, less communication, may underutilize CPU
        
- Example:
    

|Task Size|Pros|Cons|
|---|---|---|
|Fine-grained|Better load balancing|Higher synchronization overhead|
|Coarse-grained|Less communication|Potential idle processors|

---

### 2.2 Databases

- **Data granularity**: Size of data units for transactions or locking
    
    - **Row-level lock** → fine-grained, allows concurrency
        
    - **Table-level lock** → coarse-grained, simple but limits concurrency
        
- Example:
    

Fine-grained: Lock only a single bank account record  
Coarse-grained: Lock the entire accounts table

---

### 2.3 Memory & Storage

- **Memory granularity**: Smallest allocatable unit of memory (e.g., byte, word, page)
    
- **Disk block granularity**: Size of blocks read/written on disk
    
    - Fine-grained: smaller blocks, more I/O operations
        
    - Coarse-grained: larger blocks, more efficient sequential access
        

---

### 2.4 Software Design

- **Module granularity**: Size of modules/components in a system
    
    - Fine-grained modules → more modular, easier to test
        
    - Coarse-grained modules → simpler, fewer interactions
        

---

## 3️⃣ Pros and Cons of Granularity

|Type|Pros|Cons|
|---|---|---|
|Fine-grained|More parallelism, modularity, precise control|More overhead, complexity, synchronization cost|
|Coarse-grained|Simpler, less overhead|Less flexibility, less parallelism, potential underutilization|

---

## 4️⃣ Visual Example (Parallel Tasks)

Fine-grained:    [T1][T2][T3][T4][T5][T6][T7][T8]  (many small tasks)  
Coarse-grained:  [T1-----][T2-----]                    (few large tasks)

- Fine → better load balancing but more communication
    
- Coarse → less communication but may leave processors idle
    

---

## 5️⃣ Key Points for Exam / Interview

- **Granularity = level of detail or size of the smallest unit**
    
- Fine-grained → smaller, more detailed units
    
- Coarse-grained → larger, less detailed units
    
- Context-specific: parallel computing, databases, memory, software modules
    
- Trade-off between **control vs overhead**