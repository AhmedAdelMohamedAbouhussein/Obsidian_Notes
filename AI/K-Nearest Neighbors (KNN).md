### Meaning

**K-Nearest Neighbors (KNN)** is a **simple machine learning algorithm** used for **classification and regression**.

- It predicts the **label/value of a point** based on the labels/values of its **k closest neighbors** in the dataset.
    

---

## 1. How KNN Works

1. Choose a value for **k** (number of neighbors to consider).
    
2. Calculate the **distance** between the new point and all points in the training data.
    
    - Common distances: **Euclidean, Manhattan**
        
3. Identify the **k nearest neighbors** (closest points).
    
4. Prediction:
    
    - **Classification:** Choose the **majority class** among neighbors
        
    - **Regression:** Take the **average value** of neighbors
        

---

## 2. Key Features

- **Lazy Learning:** Does not train a model in advance; computation happens during prediction
    
- **Non-parametric:** Makes **no assumption about data distribution**
    
- Sensitive to **scale of features** → normalization often needed
    

---

## 3. Use Cases

- Handwriting recognition
    
- Image classification
    
- Recommender systems
    
- Medical diagnosis
    

---

## 4. Memory Hook

- Think: **“Ask your neighbors what class/value to be”**
    
- KNN = “vote of the closest k points”
    

---

## 5. One-Line Exam Answer

> K-Nearest Neighbors is an algorithm that predicts the class or value of a point based on the majority or average of its k closest neighbors in the dataset.