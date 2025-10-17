The **History API** is part of the **HTML5** specification.  
It allows JavaScript to **manipulate the browser’s session history** — that’s the list of pages you can navigate through with **Back** and **Forward** buttons — **without reloading the page**.

This is what enables **Single Page Applications (SPAs)** to change URLs smoothly while staying on the same page.

---

## 📦 What It Lets You Do

|Method / Event|Purpose|
|---|---|
|`history.pushState()`|Add a new entry to the browser history|
|`history.replaceState()`|Modify the current entry (no new history added)|
|`history.back()`|Go to the previous history entry|
|`history.forward()`|Go to the next history entry|
|`history.go(n)`|Go `n` steps forward/backward|
|`window.onpopstate`|Event that triggers when the user navigates using Back/Forward|

---

## ⚙️ Example — Changing URL Without Reloading

![[Pasted image 20251018003010.png]]

1. When you click a button:
    
    - The URL changes (e.g., `/about`)
        
    - The page content changes — **but no reload happens**
        
2. If you press the browser’s **Back** button:
    
    - The `onpopstate` event fires
        
    - JavaScript updates the page content accordingly
        

---

## 🧭 Methods in Detail

### 1. `history.pushState(state, title, url)`

Adds a new history entry.

`history.pushState({ page: "about" }, "", "/about");`

- `state`: a JS object you can retrieve later (for restoring page state)
    
- `title`: mostly ignored by browsers (keep it empty)
    
- `url`: the new URL to show
    

---

### 2. `history.replaceState(state, title, url)`

Replaces the current entry instead of adding a new one.

`history.replaceState({ page: "home" }, "", "/");`

---

### 3. `window.onpopstate`

Triggered when user navigates using Back/Forward buttons.

`window.onpopstate = (event) => {   console.log("Back/Forward pressed!", event.state); };`

---

## 📈 Why It’s Useful

- ✅ Create **SPAs (Single Page Applications)**
    
- ✅ Update the **address bar** without reloading
    
- ✅ Maintain **browser navigation (Back/Forward)**
    
- ✅ Store **page state** in the URL for sharing/bookmarks
    

---

## ⚠️ Notes

- The URL you set **must be same-origin** (same domain).
    
- The new URL won’t trigger a real HTTP request — it’s **client-side only**.
    
- If the user refreshes the page, the browser will make a **normal request** to that URL.
    

---

### 🧩 Real-life Example

Frameworks like **React Router**, **Vue Router**, and **Angular Router** all use the **History API** underneath to handle navigation between components.

---

✅ **In short:**

> The **History API** lets JavaScript change the browser’s URL and navigation history — without reloading the page — enabling smooth, app-like web experiences.