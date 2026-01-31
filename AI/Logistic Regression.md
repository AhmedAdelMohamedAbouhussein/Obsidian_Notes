### Meaning

**Logistic Regression** is a **statistical/machine learning method** used to model the **probability of a binary outcome** (yes/no, 0/1, true/false) based on one or more independent variables.

- Unlike linear regression, the output is **between 0 and 1** (probability).
    
- Often used for **classification tasks**.
    

---

## 1. How It Works

- Uses the **logistic (sigmoid) function** to map any value to a probability:
    

σ(z)=11+e−z\sigma(z) = \frac{1}{1 + e^{-z}}σ(z)=1+e−z1​

- Where `z = b0 + b1*x1 + b2*x2 + ... + bn*xn`
    
- Prediction:
    
    - If probability ≥ 0.5 → class 1
        
    - If probability < 0.5 → class 0
        

---

## 2. Key Concepts

- **Binary Classification:** Two classes (0/1)
    
- **Odds & Logit:** Logistic regression models the **log-odds** of the outcome
    
- **Coefficients:** Show how each feature affects the probability of the outcome
    

---

## 3. Use Cases

- Email spam detection (spam/not spam)
    
- Customer churn prediction (leave/stay)
    
- Medical diagnosis (disease/no disease)
    
- Loan approval (approve/deny)
    

---

## 4. Memory Hook

- Think: **“Predict yes/no using probabilities”**
    
- Logistic Regression = **linear model + sigmoid → probability → class**
    

---

## 5. One-Line Exam Answer

> Logistic Regression is a method for predicting the probability of a binary outcome using one or more independent variables, mapping results through a sigmoid function.