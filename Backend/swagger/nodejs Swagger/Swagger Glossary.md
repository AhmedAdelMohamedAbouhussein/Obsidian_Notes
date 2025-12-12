# 📚 Swagger/OpenAPI Glossary for Notes

## 1️⃣ **OpenAPI version**

- **Key:** `openapi`
    
- **Description:** The version of the OpenAPI/Swagger specification your file is using.
    
- **Example:**
    

`"openapi": "3.0.0"`

---

## 2️⃣ **Info**

- **Key:** `info`
    
- **Description:** Metadata about your API. Includes the **title**, **version**, **description**, and optionally **contact** or **license**.
    
- **Example:**
    

![[Pasted image 20251110173856.png]]

---

## 3️⃣ **Servers**

- **Key:** `servers`
    
- **Description:** Defines the base URL(s) where your API is hosted. Can include multiple environments (dev, staging, production).
    
- **Example:**
    

![[Pasted image 20251110173903.png]]
---

## 4️⃣ **Paths**

- **Key:** `paths`
    
- **Description:** The **core of the API** — lists all endpoints (routes), their methods (`GET`, `POST`, etc.), parameters, request bodies, and responses.
    
- **Example:**
    

![[Pasted image 20251110173911.png]]
---

## 5️⃣ **HTTP Methods**

- **Keys:** `get`, `post`, `put`, `patch`, `delete`, `options`, `head`
    
- **Description:** Standard HTTP methods describing the type of operation.
    
    - `GET`: Retrieve data
        
    - `POST`: Create new data
        
    - `PUT`: Replace data
        
    - `PATCH`: Partially update data
        
    - `DELETE`: Remove data
        
    - `OPTIONS`: Describe communication options
        
    - `HEAD`: Retrieve headers only
        

---

## 6️⃣ **Summary & Description**

- **Key:** `summary`, `description`
    
- **Description:**
    
    - `summary`: Short one-line explanation of the endpoint
        
    - `description`: Longer explanation, can include details, warnings, or examples
        
- **Example:**
    

![[Pasted image 20251110173925.png]]

---

## 7️⃣ **Tags**

- **Key:** `tags`
    
- **Description:** Group endpoints into categories. Useful in Swagger UI for navigation.
    
- **Example:**
    

`tags: ["Users"]`

---

## 8️⃣ **Parameters**

- **Key:** `parameters`
    
- **Description:** Inputs that come **from the URL or query string**, not the body. Can be:
    
    - `path` → part of the URL (`/users/{id}`)
        
    - `query` → query string (`?page=2&limit=10`)
        
    - `header` → HTTP headers (`Authorization: Bearer ...`)
        
    - `cookie` → cookies
        
- **Example:**
    

![[Pasted image 20251110173935.png]]

---

## 9️⃣ **Request Body**

- **Key:** `requestBody`
    
- **Description:** The **data the client sends** in the body of `POST`, `PUT`, or `PATCH` requests. Can include `required` fields and `properties`.
    
- **Example:**
    

![[Pasted image 20251110173943.png]]

---

## 🔟 **Required**

- **Key:** `required`
    
- **Description:** Indicates **mandatory fields** for `requestBody` or object `properties`.
    
- **Example:**
    

`required: [email, password]`

---

## 1️⃣1️⃣ **Properties**

- **Key:** `properties`
    
- **Description:** Fields in an object (`requestBody` or `response`). Defines **field type**, **example**, and optional **enum** for allowed values.
    
- **Example:**
    
![[Pasted image 20251110173955.png]]

---

## 1️⃣2️⃣ **Schema**

- **Key:** `schema`
    
- **Description:** Defines the **structure and type** of data for `parameters`, `requestBody`, or `responses`. Often references `components.schemas`.
    
- **Example:**
    

`schema:   $ref: '#/components/schemas/UserRequest'`

---

## 1️⃣3️⃣ **Responses**

- **Key:** `responses`
    
- **Description:** What the API **returns** after a request. Each HTTP status code (`200`, `404`, etc.) can have its own schema and description.
    
- **Example:**
    

![[Pasted image 20251110174008.png]]

---

## 1️⃣4️⃣ **Components**

- **Key:** `components`
    
- **Description:** Store **reusable schemas, parameters, responses, and security schemes**.
    
- **Example:**
    

![[Pasted image 20251110174016.png]]

---

## 1️⃣5️⃣ **Schemas**

- **Key:** `schemas` (inside `components`)
    
- **Description:** Define **reusable object models**. Can be used in `requestBody` and `responses`.
    
- **Example:**
    

![[Pasted image 20251110174024.png]]

---

## 1️⃣6️⃣ **Examples**

- **Key:** `example`
    
- **Description:** Provides sample data for fields in `requestBody`, `parameters`, or `responses`.
    
- **Example:**
    

![[Pasted image 20251110174032.png]]

---

## 1️⃣7️⃣ **Enums**

- **Key:** `enum`
    
- **Description:** Restrict a string or number field to **predefined values**.
    
- **Example:**
    

![[Pasted image 20251110174039.png]]

---

## 1️⃣8️⃣ **Security**

- **Key:** `security`
    
- **Description:** Define **authentication requirements** per endpoint. Can reference `components.securitySchemes`.
    
- **Example:**
    

`security:   - bearerAuth: []`

---

## 1️⃣9️⃣ **AllOf / OneOf / AnyOf**

- **Keys:** `allOf`, `oneOf`, `anyOf`
    
- **Description:** Combine multiple schemas:
    
    - `allOf`: Must match **all** schemas
        
    - `oneOf`: Must match **exactly one**
        
    - `anyOf`: Must match **at least one**
        

---

## 2️⃣0️⃣ **Tags at Components Level**

- **Purpose:** Reuse tags across endpoints and describe them in one place.
    
- **Example:**
    

`tags:   - name: Users     description: Endpoints to manage users`

---

## 2️⃣1️⃣ **Deprecated**

- **Key:** `deprecated`
    
- **Description:** Marks an endpoint or field as **no longer recommended for use**. Swagger UI will usually strike it out.
    

---

## ✅ Tips for Notes

- Parameters → in URL/query/header/cookie
    
- Request body → data client sends
    
- Responses → data server returns
    
- Components → reusable objects
    
- Examples → help visualize requests & responses