# **1️⃣ What is a PyTorch tensor?**

- A **tensor** is the main data structure in PyTorch.
    
- Think of it as a **generalization of vectors and matrices** to **higher dimensions**.

| Dimension   | Example             | Shape                                   |
| ----------- | ------------------- | --------------------------------------- |
| 0D (scalar) | `5`                 | `()`                                    |
| 1D (vector) | `[1, 2, 3]`         | `(3,)`                                  |
| 2D (matrix) | `[[1,2],[3,4]]`     | `(2,2)`                                 |
| 3D          | Image with channels | `(3, 224, 224)`                         |
| 4D          | Batch of images     | `(batch_size, channels, height, width)` |
|             |                     |                                         |

- Essentially: **a tensor is an N-dimensional array**, compatible with GPU acceleration.

---

# **2️⃣ Why PyTorch uses tensors**

- Tensors can be operated on **on CPU or GPU** for fast computations.
    
- They are **similar to NumPy arrays**, but support **automatic differentiation** (gradients).
    
- Neural networks in PyTorch take **tensors as input** and output **tensors**.

---

# **3️⃣ Example: Image as a tensor**

Suppose you have a color image:

- Height = 224, Width = 224, Channels = 3 (RGB)
    
- PIL image shape: `(224, 224, 3)`
    
- PyTorch tensor shape: `(3, 224, 224)`
![[Pasted image 20251201014707.png]]

- Pixel values are converted from integers `0–255` → floats `0.0–1.0`
    
- Channels come first in PyTorch: `(C, H, W)`

---

# **4️⃣ Operations on tensors**

Tensors support all kinds of math operations:
![[Pasted image 20251201014732.png]]


# **5️⃣ Tensor in Neural Networks**

- Inputs → tensors
- Outputs → tensors
- Hidden states / embeddings → tensors
- Gradients → tensors
    

Example in your project:
![[Pasted image 20251201014758.png]]

# ✅ **Summary**

- PyTorch tensor = N-dimensional array with fast computation + gradient support.
- Tensors are the **core data type** for all neural network operations.
- For images: `(channels, height, width)`
- For batches: `(batch_size, channels, height, width)`