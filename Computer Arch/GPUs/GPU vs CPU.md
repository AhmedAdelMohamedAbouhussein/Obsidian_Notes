# 🧠 GPU vs CPU — Detailed Notes

## 1. **Definition**

| Component                          | Meaning                                                                                                                                                                       |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **CPU (Central Processing Unit)**  | The _general-purpose brain_ of the computer. Handles most tasks required by the operating system and applications.                                                            |
| **GPU (Graphics Processing Unit)** | A _specialized processor_ designed to handle thousands of small, parallel operations — originally for graphics rendering, now also used for AI, simulations, and computation. |

---

## 2. **Architecture**

### 🖥️ **CPU Architecture**

- Few **high-performance cores** (usually 4–16).
    
- Each core is **optimized for sequential (serial)** tasks.
    
- Large cache and complex control logic.
    
- Excellent at **task switching**, **branch prediction**, and **I/O operations**.
    

### 🎮 **GPU Architecture**

- Contains **hundreds or thousands of smaller cores**.
    
- Designed for **massive parallelism** — executing the same instruction on many data points simultaneously (SIMD/SIMT).
    
- Much higher **throughput** than a CPU but lower **per-core speed**.
    
- Simpler control logic and smaller caches per core.
    

---

## 3. **Main Purpose**

| CPU                                                                               | GPU                                                                                |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Handles all general system operations and instructions.                           | Processes large amounts of data in parallel — ideal for graphics and computations. |
| Good for tasks like system management, file handling, and logic-heavy operations. | Good for rendering, AI training, physics simulations, image/video processing, etc. |

---

## 4. **Performance Focus**

- **CPU:** Low latency (responds quickly to a single task).
    
- **GPU:** High throughput (handles many tasks at once).
    

Example:

- CPU → Running a word processor, managing OS tasks.
    
- GPU → Drawing each pixel of a 4K frame or training neural networks with millions of parameters.
    

---

## 5. **Parallelism Type**

|CPU|GPU|
|---|---|
|Few powerful cores → **Parallelism at task level**|Thousands of lightweight cores → **Parallelism at data level**|
|Great for different tasks at once|Great for doing the same task across large datasets|

---

## 6. **Use Cases**

|CPU|GPU|
|---|---|
|Operating systems, apps, compilers, browsers, databases|Gaming, rendering, AI/ML, cryptocurrency mining, 3D modeling, video encoding|

---

## 7. **Example Analogy**

> - A **CPU** is like a **few brilliant workers** who can handle complex, varied tasks.
>     
> - A **GPU** is like **a massive team of simple workers**, each doing small parts of a large job simultaneously.
>     

---

## 8. **Combined Usage**

Modern systems use **both together**:

- CPU handles logic, control, and sequential tasks.
    
- GPU handles parallel computation.
    

➡️ Frameworks like **CUDA**, **OpenCL**, **TensorRT**, and **DirectCompute** enable CPUs to delegate heavy parallel work to GPUs.

---

## 9. **Summary Table**

| Feature     | CPU                   | GPU                                |
| ----------- | --------------------- | ---------------------------------- |
| Cores       | 4–16                  | Hundreds to thousands              |
| Clock Speed | Higher (3–5 GHz)      | Lower (1–2 GHz)                    |
| Cache       | Large                 | Small                              |
| Strength    | Versatility & control | Parallel processing                |
| Best for    | General computing     | Graphics, AI, scientific workloads |
