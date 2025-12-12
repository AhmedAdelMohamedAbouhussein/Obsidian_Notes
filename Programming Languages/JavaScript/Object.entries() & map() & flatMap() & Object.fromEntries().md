# JavaScript Iteration Helpers Explained

## 1️⃣ `Object.entries()`

- **Purpose:** Convert an object into an array of `[key, value]` pairs.
    
- **Why:** You cannot `.map()` or `.sort()` directly on an object.
    
- **Example:**
![[Pasted image 20251127225911.png]]
---

## 2️⃣ `map()`

- **Purpose:** Loop over an array and return a **new array** of the same length.
    
- **Example:**
![[Pasted image 20251127225924.png]]

- **Use case:** Transform each item in an array into something else (like a React component).


---

## 3️⃣ `flatMap()`

- **Purpose:** `map()` + flatten nested arrays into a single array.
    
- **Example:**
![[Pasted image 20251127225940.png]]`

- **Use case:** When each iteration produces multiple items, but you want **one flat list** instead of arrays of arrays.
    
---

## 4️⃣ `Object.fromEntries()`

- **Purpose:** Convert an array of `[key, value]` pairs back into an object.
    
- **Example:**
![[Pasted image 20251127230027.png]]

- **Use case:** Convert Maps (or array entries) into JSON-safe objects for the frontend.
    

---

## 🔹 Example in Context (Your Owned Games)

### Original nested object:

![[Pasted image 20251127230037.png]]

### Convert to single array for global sort:

![[Pasted image 20251127230044.png]]

### Resulting array:

![[Pasted image 20251127230053.png]]

- **Step 1:** `Object.entries(ownedGames)` → loop platforms
    
- **Step 2:** `flatMap()` → merge arrays from all platforms into one
    
- **Step 3:** `.map()` → extract game data and add platform/gameId fields
    

---

## ✅ Summary Table

| Function               | Input                  | Output                  | Use Case                      |
| ---------------------- | ---------------------- | ----------------------- | ----------------------------- |
| `Object.entries()`     | Object                 | Array of `[key, value]` | Loop or map over an object    |
| `map()`                | Array                  | Array                   | Transform each item in array  |
| `flatMap()`            | Array                  | Flat array              | Map + flatten multiple arrays |
| `Object.fromEntries()` | Array of `[key,value]` | Object                  | Convert back to an object     |