### ⚙️ **Statically Typed Languages**

- **Definition:**  
    The type of each variable (like `int`, `string`, `float`) is **known at compile time** — before the program runs.
    
- You **must declare** the type or the compiler can infer it, but it **doesn’t change** later.
    

#### ✅ Example (Java / C / C++)

int x = 10;     // x is always an integer 
x = "Hello";    // ❌ Error! Can't assign a string to an int`

**Key points:**

- Type checking happens **before execution** (compile-time).
    
- Fewer runtime type errors.
    
- Slightly more code to write (need to declare types).
    
- Usually **faster** at runtime.
    

---

### 🧠 **Dynamically Typed Languages**

- **Definition:**  
    The type of each variable is **known at runtime**, not at compile time.
    
- You **don’t declare** variable types — they can change during execution.
    

#### ✅ Example (Python / JavaScript)

x = 10       # x is an integer 
x = "Hello"  # ✅ Now x is a string`

**Key points:**

- Type checking happens **while running** (runtime).
    
- Easier and quicker to write.
    
- Can lead to **type-related runtime errors**.
    
- Usually **slower** because type checking happens on the fly.
    

---

### ⚖️ **Comparison Table**

|Feature|Statically Typed|Dynamically Typed|
|---|---|---|
|Type known|At compile time|At runtime|
|Type declaration|Required|Not required|
|Performance|Faster|Slower|
|Errors detected|Before running|During running|
|Examples|Java, C, C++, Swift|Python, JavaScript, Ruby|

---

### 💡 In short:

- **Statically typed:** “I must know what I am before running.”
    
- **Dynamically typed:** “I’ll figure out what I am when I run.”