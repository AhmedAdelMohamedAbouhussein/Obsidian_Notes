## 🔍 What Is URL Fragmentation?

**URL fragmentation** means using the part of a URL that comes **after the `#` symbol** — called the **fragment identifier**.

It looks like this:

`https://example.com/page#section1                            
						   ↑          
						this part is the fragment`

The fragment (everything after `#`) is **not** sent to the server — it’s only used **by the browser or client-side JavaScript**.

---

## 🧠 Key Idea

The **fragment** identifies a **specific part** or **state** _within the same page_, not a new page.

It tells the browser _where to scroll_ or _which content to display_.

---

## 📘 Basic Example – HTML Anchors

If your HTML has:

`<h2 id="about">About Us</h2>`

You can link to it like:

`<a href="#about">Go to About section</a>`

When clicked, the browser scrolls to the element with that `id`.

URL changes to:

`https://example.com/page#about`

But — ✅ **no reload happens**  
The fragment is handled _entirely by the browser_.

---

## ⚙️ In JavaScript

You can **get**, **set**, or **listen to** the fragment using the `window.location` object.

### ▶️ Get current fragment:

`console.log(window.location.hash);  // Example output: "#about"`

### ▶️ Change the fragment (no reload):

`window.location.hash = "contact"; // URL becomes: https://example.com/page#contact`

### ▶️ React to fragment changes:

`window.addEventListener("hashchange", () => {   console.log("New hash:", window.location.hash); });`

This lets you make **simple single-page navigation** without frameworks — called **hash-based routing**.

---

## 🧩 Hash-Based Routing Example

![[Pasted image 20251018003226.png]]

This example:

- Uses the **fragment** (`#home`, `#about`, `#contact`) to show different content.
    
- Changes what’s displayed without reloading the page.
    
- This is **URL fragmentation in action**.
    

---

## ⚖️ URL Fragmentation vs History API

| Feature          | URL Fragment (`#...`)      | History API             |
| ---------------- | -------------------------- | ----------------------- |
| Example URL      | `/page#about`              | `/page/about`           |
| Uses `#`?        | ✅ Yes                      | ❌ No                    |
| Triggers reload? | ❌ No                       | ❌ No                    |
| Sent to server?  | ❌ No                       | ✅ Yes (on reload)       |
| Event listener   | `hashchange`               | `popstate`              |
| Typical use      | Anchor links, hash routing | SPAs (React, Vue)       |
| Complexity       | Simple                     | More control & advanced |

---

✅ **In short:**

> **URL fragmentation** means adding or changing the `#fragment` part of a URL to identify or navigate to a specific section of a page — without reloading it.