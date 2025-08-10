**JWT** stands for **JSON Web Token**. It is an open standard (**RFC 7519**) that defines a compact and self-contained way for securely transmitting information between parties as a **JSON object**. It is widely used for **authentication** and **authorization** in modern web applications.

### 🔑 Common Use Cases

1. **Authentication**: After a user logs in, the server creates a JWT and sends it to the client. The client then includes this token in the header of future requests.
2. **Authorization**: JWTs can carry roles and permissions so APIs can decide what the user is allowed to do.

### What is `jwt-decode`?
`jwt-decode` is a **JavaScript library** that allows you to decode **JWTs (JSON Web Tokens)** without verifying the signature.

### Purpose:

It extracts the **payload** (data inside the token) such as the user ID, name, email, etc., from a JWT string, so you can use it in your frontend.