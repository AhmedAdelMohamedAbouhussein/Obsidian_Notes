## **1️⃣ swagger-jsdoc**

**Purpose:**

- Generates a **Swagger/OpenAPI JSON specification** automatically by reading your **JSDoc comments** in your code.
    
- You write structured comments in your route files describing your API endpoints, parameters, and responses, and it outputs a machine-readable OpenAPI spec.
    

**Key Features:**

- Supports **OpenAPI 3.0**.
    
- Reads multiple files via globs (e.g., `"./routes/*.js"`).
    
- Converts comments like this:
- ![[Pasted image 20251110174219.png]]

![[Pasted image 20251110174239.png]]

## **2️⃣ swagger-ui-express**

**Purpose:**

- Serves your **Swagger JSON spec** as an interactive **web page** where you can test endpoints.
    
- Lets you **execute API requests directly from the browser**, see responses, headers, and descriptions.
    

**Key Features:**

- Easy integration with Express (`app.use()`).
    
- No frontend coding needed—everything is generated automatically from your Swagger spec.
    
- Can show authentication, parameters, request bodies, and responses.
    

**Usage Example:**

![[Pasted image 20251110174253.png]]
- Visit `http://localhost:3000/api-docs` to see a fully interactive API documentation page.
    

---

### ✅ **How They Work Together**

1. `swagger-jsdoc` → **converts JSDoc comments to OpenAPI JSON**.
    
2. `swagger-ui-express` → **renders the JSON as a live, interactive documentation page**.