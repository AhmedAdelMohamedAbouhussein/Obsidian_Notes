# **Flask: Web Framework in Python**

**Flask** is a **lightweight web framework** for Python.  
It allows you to **build web applications and APIs** easily.

---

### **Key Points**

1. **Web server:**
    
    - Flask runs a **local server** on your computer (or on a cloud server).
        
    - Handles incoming HTTP requests from browsers or other clients.
        
2. **Routing:**
    
    - You define **routes** (URLs) using `@app.route("/some_path")`.
        
    - Each route is linked to a Python function that **returns a response**.
        
3. **Responses:**
    
    - Can return **HTML**, **JSON**, or **files**.
        
    - Example:
        
        - `jsonify(data)` → JSON response
            
        - `send_from_directory("images", name)` → file (like image)
            
4. **Dynamic endpoints:**
    
    - Flask allows **parameters in URLs**.
        
    - Example: `/image/<name>` → `<name>` can be anything, like `cat.png`.
        
5. **Debug mode:**
    
    - `app.run(debug=True)` → automatically reloads code changes and shows error messages.