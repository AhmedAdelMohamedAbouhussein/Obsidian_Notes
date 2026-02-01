# React Diffing

### Meaning

In React, **diffing** is the process React uses to **efficiently update the DOM** by comparing the **previous virtual DOM** with the **new virtual DOM** and applying only the **necessary changes**.

This is also called **reconciliation**.

---

## 1. How It Works

1. React keeps a **Virtual DOM (VDOM)** in memory.
    
2. When a component’s state or props change:
    
    - React creates a **new virtual DOM** tree.
        
3. React **diffs** the new VDOM against the previous VDOM:
    
    - Compares old vs new nodes
        
    - Determines the minimal set of changes
        
4. React updates the **real DOM** **only where necessary**.
    

---

## 2. Why Diffing Matters

- DOM updates are **slow**.
    
- Directly updating the DOM for every change is **inefficient**.
    
- Diffing + Virtual DOM makes React **fast**, even for large applications.
    

---

## 3. How React Optimizes Diffing

### Key Strategies

1. **Element Type Check**
    
    - If element type changes → replace entire subtree
        
    - Example: `<div>` → `<span>` → replace node
        
2. **Keyed Lists**
    
    - For lists, React uses **keys** to match elements efficiently
        
    - Avoids unnecessary re-renders
        
3. **Component-level Diff**
    
    - Only components affected by state/props changes are diffed
        

---

## 4. Example
![[Pasted image 20260131130431.png]]
- When `count` changes:
    
    - React creates a **new VDOM** for `<h1>{count}</h1>`
    - Diffs it with the previous VDOM
    - Updates **only the `<h1>` text**, not the `<button>` or `<div>`.

---

## 5. Memory Hook

- **React diffing = smart comparison**
- Think: “Compare old virtual DOM → update only what changed → save performance”    

---

## 6. One-Line Exam Answer

> In React, diffing is the process of comparing the previous and new virtual DOM to determine the minimal changes needed to update the real DOM efficiently.
