### ✅ **1xx: Informational**

- **100 Continue** – Request received, continue sending the body.
- **101 Switching Protocols** – Server is switching protocols (e.g., to WebSocket).
- **102 Processing** – Server has received and is processing the request.

---

### 🟢 **2xx: Success**

- **200 OK** – Request succeeded.
- **201 Created** – Resource created (often in response to `POST` or `PUT`).
- **202 Accepted** – Request accepted but not yet processed.
- **204 No Content** – Request succeeded, no content in response.

---

### 🟡 **3xx: Redirection**

- **301 Moved Permanently** – Resource moved to a new URL.
- **302 Found (Temporary Redirect)** – Resource temporarily at a different URI.
- **304 Not Modified** – Client can use cached data.

---

### 🔴 **4xx: Client Errors**

- **400 Bad Request** – Invalid request from the client.
- **401 Unauthorized** – Authentication required or failed.
- **403 Forbidden** – You are not allowed to access the resource.
- **404 Not Found** – Resource not found.
- **405 Method Not Allowed** – HTTP method (e.g., POST, GET) not allowed for the endpoint.
- **409 Conflict** – Request could not be processed due to a conflict (e.g., duplicate data).
- **422 Unprocessable Entity** – Syntax is correct, but semantics are wrong (often used in validation).
- **429 Too Many Requests** – Rate limit exceeded.

---

### 🔥 **5xx: Server Errors**

- **500 Internal Server Error** – Generic server error.
- **501 Not Implemented** – Server doesn't support the functionality.
- **502 Bad Gateway** – Invalid response from an upstream server.
- **503 Service Unavailable** – Server temporarily unavailable (e.g., maintenance).
- **504 Gateway Timeout** – Upstream server took too long to respond.