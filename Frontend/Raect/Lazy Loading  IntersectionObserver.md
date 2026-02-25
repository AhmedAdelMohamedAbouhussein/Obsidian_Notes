### 🔹 `const observer = new IntersectionObserver(...)`

- `IntersectionObserver` is a browser API.
- It "watches" an element (your card) and tells you when it comes into the viewport.
- This lets you defer loading/rendering heavy content until the user actually scrolls near it → **lazy loading**.

---

### 🔹 `entries.forEach((entry) => { ... })`

Each `entry` represents an element being observed.

- `entry.isIntersecting` → **true** if your card is at least partly visible on the screen.
    
- When true:
    
    - `setIsVisible(true)` → tells React: "Now load/show this card."
    - `observer.disconnect()` → stop observing after the first time (so the card loads only once).

---

### 🔹 `{ threshold: 0.2 }`

This means the callback runs when **20% of the card** is visible on screen.

- If you set it to `1.0`, it waits until the whole card is visible.
- If `0`, it triggers as soon as _any_ pixel of the card appears.

---

### 🔹 `observer.observe(cardRef.current)`

This starts watching the **card DOM element** that you referenced with `ref={cardRef}`.

---

### 🔹 `return () => { observer.unobserve(...) }`

Cleanup function → makes sure you **stop watching** the card if the component unmounts.  
(Prevents memory leaks.)

---

### 🔹 `ref={cardRef}`

This attaches a **reference** to the card’s DOM node so the `IntersectionObserver` knows exactly what to watch.

---

### 🔹 `<img src={image} alt={...} loading="lazy" />`

- The **`loading="lazy"`** attribute is HTML’s **built-in lazy loading** for images.
- The browser automatically delays downloading this image until it’s almost visible.
- Saves bandwidth & speeds up initial page load.

---

✅ **In summary**:

- `IntersectionObserver` → Lazy loads your **React components/cards**.
    
- `loading="lazy"` → Lazy loads **images** inside those cards.  
    Together, they make sure you **don’t render or download things until needed**, improving performance.
    
![[Pasted image 20250829171559.png]]