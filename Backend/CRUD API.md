A **CRUD API** is an API (Application Programming Interface) that allows clients to **Create, Read, Update, and Delete** resources. Each letter in CRUD corresponds to a type of operation:

---

### **1️⃣ Create**
- Adds a new resource.
- Usually mapped to **HTTP POST**.
- Example: Add a new user to the database.
### **2️⃣ Read**
- Retrieves resource(s) from the database.
- Usually mapped to **HTTP GET**.
### **3️⃣ Update**
- Modifies an existing resource.
- Usually mapped to **HTTP PUT** or **PATCH**.
- Example: Update a user’s name.
### **4️⃣ Delete**
- Removes a resource (or marks it as deleted).
- Usually mapped to **HTTP DELETE**.
- Example: Delete a user by ID.

| CRUD   | HTTP Method | Description              |
| ------ | ----------- | ------------------------ |
| Create | POST        | Add a new resource       |
| Read   | GET         | Fetch resource(s)        |
| Update | PUT/PATCH   | Modify existing resource |
| Delete | DELETE      | Remove resource          |
