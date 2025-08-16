`passport.js` (or just **Passport**) is a **popular authentication middleware** for **Node.js** and **Express** apps.

### 🔑 What it does

- Helps you add **login systems** easily.
- Works with many different authentication methods (called **strategies**).
- Handles things like sessions, redirects, and verifying users.
- Keeps your app’s core code clean by abstracting login details.

---

### ⚙️ How it works

1. You configure Passport in your Express app.
2. You choose which **strategy** you want to use for authentication, e.g.:
    - `passport-local` → email/username + password
    - `passport-google-oauth20` → Google login
    - `passport-steam` → Steam login
    - `passport-facebook`, `passport-github2`, etc.
3. Passport takes care of redirecting users, checking credentials, and then returning a **user object**.
4. You decide what to do with that user (store in database, create session, etc.).