## **1. Cookies**

- **Definition:** Small pieces of data stored **on the client’s browser**.
    
- **Where they live:** Browser (or sometimes other clients).
    
- **Purpose:** Store information you want to persist across requests, like a session ID, theme preference, or auth token.
    
- **Key properties:**
    
    - `httpOnly` → prevents client-side JavaScript from reading the cookie (safer from XSS attacks).
    - `maxAge` or `expires` → controls how long the cookie stays in the browser.
    - `secure` → only sent over HTTPS.
    
- **Pros:** Fast, stored on the client, works across requests.
- **Cons:** Limited size (~4KB per cookie), can be manipulated if not httpOnly/secure.

## **2. Sessions**

- **Definition:** Server-side storage of user data, usually linked to a **session ID** that is stored in a cookie on the client.
- **Where they live:** On the server (database, memory, or file).
- **Purpose:** Keep track of user state between requests (like login status, shopping cart).
    
- **How it works:**
    
    1. User logs in.
    2. Server creates a session (in memory, MongoDB, Redis, etc.) and generates a **session ID**.
    3. Server sends a cookie to the client with that session ID.
    4. On each request, the client sends the cookie, server looks up the session, and knows who the user is.

- **Pros:** Can store more data than cookies, safer (sensitive data stays on the server).
- **Cons:** Requires server storage; can’t share across domains without special setup.

## **3. How They Work Together**

1. **Cookie stores only the session ID**.
2. **Server stores the actual session data**.
3. Example flow:

| Step | Action                                                                                     |
| ---- | ------------------------------------------------------------------------------------------ |
| 1    | User logs in. Server creates session `{ userId: 123 }` and sends cookie `sessionId=abc123` |
| 2    | User makes a request. Browser sends `sessionId=abc123` cookie                              |
| 3    | Server looks up `abc123` in session store and retrieves `{ userId: 123 }`                  |
| 4    | Server knows who the user is and responds accordingly                                      |

### **4. Key Differences**

|Feature|Cookie|Session|
|---|---|---|
|Stored on|Client|Server|
|Can store sensitive data?|No (not safe)|Yes (safe on server)|
|Lifespan|Configurable via cookie settings|Usually configurable via server TTL|
|Size limit|~4KB|Depends on server storage|
|Usage|Store small info, session ID|Store user state, cart, login info|
