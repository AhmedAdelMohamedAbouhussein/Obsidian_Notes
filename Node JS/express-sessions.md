**`express-session`** is a middleware for **Express.js** that allows you to manage **user sessions** on your server.

---
### **What a session is**

- A **session** is a way to store data **specific to a user** across multiple requests.
- Unlike HTTP, which is stateless (every request is independent), sessions let you remember things like:
    - Logged-in status
    - Shopping cart contents
    - User preferences

---
### **How `express-session` works**

1. When a user first connects, Express creates a **session object** for them.
2. A **session ID** is generated and stored in a **cookie** on the user’s browser.
3. On subsequent requests, the cookie is sent back, and Express uses the session ID to retrieve the user’s session data.
4. The session data is stored **server-side** (in memory, database, or other stores).

---
### **Key Options**

- **`secret`** – A string used to sign the session cookie (keeps it secure).
- **`resave`** – Forces session to be saved back to the store even if not modified. Usually `false`.
- **`saveUninitialized`** – Saves a new but empty session. Usually `false` to avoid storing unnecessary sessions.
- **`cookie`** – Configure the cookie properties (e.g., secure, maxAge).

![[Pasted image 20250817172622.png]]
![[Pasted image 20250817172610.png]]