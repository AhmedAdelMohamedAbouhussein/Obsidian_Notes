### Meaning

**Support Vector Machine (SVM)** is a **supervised machine learning algorithm** used for **classification** (and sometimes regression).

- It finds a **hyperplane** that **best separates classes** in the feature space.
    
- Works well for **high-dimensional data**.
    

---

## 1. How SVM Works

1. Each data point is represented in **n-dimensional space** (n = number of features).
    
2. SVM finds the **optimal hyperplane** that separates the classes.
    
    - Hyperplane = decision boundary
        
    - Goal: **maximize the margin** between the classes
        
3. **Support Vectors:** Points **closest to the hyperplane**; they define the margin.
    

---

## 2. Key Concepts

- **Margin:** Distance between the hyperplane and nearest data points
    
- **Kernel Trick:** Allows SVM to separate **non-linear data** by mapping it into higher dimensions
    
    - Common kernels: Linear, Polynomial, RBF (Radial Basis Function)
        
- **Hard Margin:** No misclassifications allowed
    
- **Soft Margin:** Allows some misclassifications for better generalization
    

---

## 3. Use Cases

- Image classification
    
- Text categorization (spam vs. non-spam emails)
    
- Handwriting recognition
    
- Bioinformatics (gene classification)
    

---

## 4. Memory Hook

- Think: **“Draw the best line (or plane) that separates the groups with the widest gap”**
    
- Support Vectors = “the points that hold the line in place”
    

---

## 5. One-Line Exam Answer

> Support Vector Machine is an algorithm that finds the optimal hyperplane to separate classes in a dataset, using support vectors to maximize the margin and optionally kernels for non-linear separation.