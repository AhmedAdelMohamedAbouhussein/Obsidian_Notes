### Meaning

**GMM** is an **unsupervised machine learning algorithm** used for **clustering and density estimation**.

- Assumes the data is generated from a **mixture of several Gaussian (normal) distributions**.
    
- Each Gaussian represents a **cluster**.
    

---

## 1. How GMM Works

1. Model assumes data comes from **k Gaussian distributions**.
    
2. Each Gaussian has **mean (μ), variance (σ²), and weight (π)**.
    
3. Uses **Expectation-Maximization (EM) algorithm** to:
    
    - Estimate which points belong to which cluster (Expectation step)
        
    - Update the Gaussian parameters to best fit the data (Maximization step)
        
4. Iterates until **convergence**.
    

---

## 2. Key Features

- **Soft Clustering:** Each point has a **probability of belonging** to each cluster, unlike KNN or K-Means (hard clustering).
    
- Can model **clusters of different shapes and sizes**, unlike K-Means which assumes spherical clusters.
    

---

## 3. Use Cases

- Image segmentation
    
- Speaker recognition / voice clustering
    
- Anomaly detection
    
- Customer segmentation
    

---

## 4. Memory Hook

- Think: **“Each cluster = a bell curve; each point can belong to multiple curves with probabilities”**
    
- GMM = “soft version of K-Means using Gaussians”
    

---

## 5. One-Line Exam Answer

> Gaussian Mixture Model (GMM) is an unsupervised algorithm that models data as a mixture of multiple Gaussian distributions and assigns probabilities of belonging to each cluster.