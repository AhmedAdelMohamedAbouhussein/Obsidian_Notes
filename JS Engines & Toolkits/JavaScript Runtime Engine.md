A **JavaScript runtime engine** is the **environment that executes JavaScript code**.

- It parses, compiles, and runs JS code.
    
- Provides **built-in functions and objects** (like `setTimeout`, `console`, `Math`, etc.).
    
- Usually embedded inside **browsers or servers** (e.g., Node.js).
    

---

## 1. Key Features

- **Interpreter + JIT compiler:** Converts JS code to machine code for execution.
    
- **Event Loop:** Handles asynchronous operations like timers, I/O, and promises.
    
- **Garbage Collection:** Automatically frees memory no longer in use.
    

---

## 2. Popular JavaScript Engines

|Engine|Used By|Notes|
|---|---|---|
|**V8**|Google Chrome, Node.js|Compiles JS to fast machine code|
|**SpiderMonkey**|Firefox|Mozilla’s engine|
|**JavaScriptCore (Nitro)**|Safari|Apple’s engine|
|**Chakra**|Old Edge|Microsoft’s engine (replaced by Chromium)|

---

## 3. How It Works (Simplified)

1. **Parse:** Reads JS code → creates Abstract Syntax Tree (AST)
    
2. **Compile / Interpret:** JIT compiler turns JS into machine code
    
3. **Execute:** Runs code, handles events asynchronously
    
4. **Memory Management:** Garbage collector cleans up unused objects
    

---

## 4. Memory Hook

- Think: **“Engine = JS brain + muscle”**
    
    - Brain → parses and understands code
        
    - Muscle → executes code fast
        

---

## 5. One-Line Exam Answer

> A JavaScript runtime engine is the environment that parses, compiles, and executes JavaScript code, providing built-in functions, asynchronous handling, and memory management.