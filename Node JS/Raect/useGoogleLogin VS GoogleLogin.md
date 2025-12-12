### 🔹 `GoogleLogin` — **Component-based**

- This is a **prebuilt component**.
- Handles the **entire login UI flow** for you.
- When the user logs in, it gives you a **JWT (ID token)**.
- You decode this JWT using `jwt-decode` to get user info (e.g., email, name, etc.).
- You **don’t** get an access token.
- Good for:
    - Basic login and signup using Google
    - When you just want user's profile info (email, name, picture)
    - No need to call other Google APIs

> **Returned data:** `credential` (which is the JWT)  
> You decode it with `jwt-decode(credential)`

![[Pasted image 20250805143515.png]]

### 🔸 `useGoogleLogin` — **Hook-based**

- This gives you **more control**.
- Instead of JWT, it gives you a **Google OAuth access token**.
- Useful if:
    - You need to call **Google APIs** (like Calendar, Gmail, YouTube)
    - You want to manage tokens manually
- It doesn't give you a JWT/ID token. 

![[Pasted image 20250805143548.png]]

![[Pasted image 20250805143755.png]]