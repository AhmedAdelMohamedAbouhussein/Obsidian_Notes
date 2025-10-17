### 🧠 **What is Big O Notation?**

**Big O Notation** describes **how fast** (or **slow**) an algorithm grows as the **input size increases**.

It doesn’t measure actual time or memory — it measures **efficiency** or **complexity**.

👉 It tells you **how the algorithm scales** when you give it _more data_.

---

### ⚙️ **Why it’s used**

- To compare algorithms’ performance.
    
- To understand if your program will still be fast when handling **large inputs**.
    
- To find **bottlenecks** in your code.
    

---

### 📈 **Common Big O Complexities**

|Big O|Name|Description|Example|
|---|---|---|---|
|**O(1)**|Constant time|Runs the same time no matter the input size|Accessing an array element|
|**O(log n)**|Logarithmic time|Grows slowly as input increases|Binary search|
|**O(n)**|Linear time|Grows directly with input size|Loop through all items|
|**O(n log n)**|Log-linear time|Slightly slower than linear|Merge sort, Quick sort|
|**O(n²)**|Quadratic time|Grows very fast with input size|Nested loops|
|**O(2ⁿ)**|Exponential time|Doubles each time input increases|Recursive Fibonacci|
|**O(n!)**|Factorial time|Extremely slow|Solving traveling salesman brute force|

---

### 📊 **Visual Growth Comparison**

`Fastest  →  O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)`

As `n` (input size) grows, the time taken by O(n²), O(2ⁿ), and O(n!) becomes huge.

---

### 🧩 **Example**

#### Example 1: O(1)

def get_first_item(arr):    
	return arr[0]`

→ Always takes the same time (constant).

---

#### Example 2: O(n)

def print_items(arr):    
	for item in arr:         
		print(item)`

→ Takes more time as the array gets larger (linear).

---

#### Example 3: O(n²)

def print_pairs(arr):     
	for a in arr:         
		for b in arr:             
			print(a, b)`

→ Every element pairs with every other element (quadratic).

---

### 🧠 **In simple words**

- **Big O** = How your code behaves as the input **gets larger**.
    
- It helps answer: “Will this program still run fast when I have 1 million items?”