In **Node.js / Express**, **middleware** is basically a **function that runs between** the moment the server **receives a request** and the moment it **sends back a response**.

Think of them as “checkpoints” or “helpers” in the request → response flow.

## **How middleware works**

A middleware function has access to:

- `req` → the request object (data from the client)
- `res` → the response object (used to send data back)
- `next` → a function that moves to the next middleware in the chain

![[Pasted image 20250811182153.png]]

## **Types of middleware**

1. **Application-level middleware**  
    Runs on every request or specific routes.
	![[Pasted image 20250811182236.png]]
2. **Router-level middleware**  
	Attached only to certain routers.
	![[Pasted image 20250811182350.png]]
3. **Built-in middleware**  
    Comes with Express (e.g. `express.static`, `express.json`).
    
4. **Third-party middleware**  
    Installed via npm (e.g. `cors`, `morgan`, `helmet`).
    
5. **Error-handling middleware**  
    Special middleware with **four arguments** `(err, req, res, next)` used to catch and handle errors.
    

---

## **Why middleware is useful**

- Logging requests
- Validating user authentication
- Parsing incoming request bodies
- Handling errors in one place
- Serving static files