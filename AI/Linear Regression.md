### Meaning

**Linear Regression** is a **statistical/machine learning method** used to model the **relationship between a dependent variable (target) and one or more independent variables (features)**.

- Assumes the relationship is **linear** (a straight line).
    
- Goal: **predict values** or **understand relationships**.
    

---

## 1. Simple Linear Regression (One Feature)

**Equation:**

y=mx+by = mx + by=mx+b

- `y` = dependent variable (what you want to predict)
    
- `x` = independent variable (input)
    
- `m` = slope (change in `y` per unit change in `x`)
    
- `b` = intercept (value of `y` when `x = 0`)
    

---

## 2. Multiple Linear Regression (Multiple Features)

**Equation:**

y=b0+b1x1+b2x2+...+bnxny = b_0 + b_1x_1 + b_2x_2 + ... + b_nx_ny=b0​+b1​x1​+b2​x2​+...+bn​xn​

- `b_0` = intercept
    
- `b_1, b_2, ..., b_n` = coefficients for each feature
    
- Models **combined effect** of multiple features on `y`
    

---

## 3. How It Works

1. Fit a **line (or hyperplane)** that minimizes the **difference between predicted and actual values**
    
2. Commonly uses **Least Squares Method**: minimizes the sum of squared errors (SSE)
    

---

## 4. Key Concepts

- **Error / Residual**: difference between actual and predicted value
    
- **R² (R-squared)**: how well the model explains the variation in `y` (0–1)
    
- **Assumptions**:
    
    1. Linear relationship between features and target
        
    2. Residuals are normally distributed
        
    3. No or little multicollinearity in features
        
    4. Homoscedasticity (constant variance of residuals)
        

---

## 5. Use Cases

- Predicting prices (house, stock)
    
- Forecasting sales or demand
    
- Trend analysis in business or economics
    

---

## 6. Memory Hook

- Think: **“Fit a straight line to predict something”**
    
- Linear Regression = **predict Y from X using a line**
    

---

## 7. One-Line Exam Answer

> Linear Regression is a method to model the linear relationship between one or more independent variables and a dependent variable to make predictions or understand trends.