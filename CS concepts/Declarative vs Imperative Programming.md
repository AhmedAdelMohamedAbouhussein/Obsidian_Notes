## 🧠 **Declarative vs Imperative Programming**

These are **two different styles (paradigms)** of writing code — they describe **how you tell the computer what to do**.

---

### ⚙️ **1. Imperative Programming**

- You tell the computer **exactly _how_** to do something, **step by step**.
    
- Focus: **How to achieve** the result.
    
- You control the **flow**, **loops**, and **variables**.

#### 🧩 Example (in Python)

`# Print all even numbers from 1 to 10 
for i in range(1, 11):    
	if i % 2 == 0:        
		print(i)`

Here, you:

- Create a loop
    
- Check each number
    
- Decide what to print
    

👉 You tell the computer _how_ to do it.

#### 🔹 Examples of Imperative Languages:

C, Java, Python (can be used imperatively), JavaScript, C++.

---

### 🧠 **2. Declarative Programming**

- You tell the computer **what you want**, not **how to do it**.
    
- Focus: **The goal or result**, not the steps.
    
- The system decides the best way to achieve it.
    

#### 🧩 Example (in SQL)

`SELECT name FROM students WHERE grade > 90;`

You don’t say **how** to search or loop — just **what you want**.

#### 🧩 Example (in HTML)

`<h1>Hello World</h1>`

You declare **what should appear**, not **how to draw it**.

---

### ⚖️ **Comparison Table**

|Feature|Imperative|Declarative|
|---|---|---|
|Focus|How to do it|What to do|
|Control flow|You define it (loops, conditions)|System handles it|
|Example languages|C, Java, Python, JavaScript|SQL, HTML, React, Prolog|
|Example code|`for`, `if`, `while`|`SELECT`, `<div>`, JSX|
|Readability|More detailed, step-by-step|More abstract, human-like|
|Advantage|Fine control over behavior|Simpler, less code|
|Disadvantage|Verbose, error-prone|Less control over internals|

---

### 💡 **Analogy**

|Type|Analogy|
|---|---|
|**Imperative**|Like giving cooking instructions: “Chop onions, fry them, then add eggs.”|
|**Declarative**|Like ordering food: “I want an omelet.” (The chef figures out how to make it.)|

---

### 🧩 Example in Web Development

|Task|Imperative (JavaScript)|Declarative (React JSX)|
|---|---|---|
|Display a message|`document.createElement('p');`  <br>`p.textContent = "Hi!";`  <br>`document.body.appendChild(p);`|`<p>Hi!</p>`|

---

### 🧭 In short:

- **Imperative** = _How_ to do it.
    
- **Declarative** = _What_ you want done.