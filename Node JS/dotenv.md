`dotenv` is a small **Node.js library** that lets you load **environment variables** from a `.env` file into your Node.js app.

In most projects, especially Express apps, you don’t want to **hard-code secrets** like:

- `PORT=3000`
- `DATABASE_URL=postgres://...`
- `JWT_SECRET=supersecret123`
- `GOOGLE_CLIENT_ID=...`

Instead, you put these in a `.env` file 
And then in your app (like `index.js`), you load them using:
![[Pasted image 20250807153936.png]]
### What’s the benefit?

- Keeps secrets/config out of your code
- Makes it easy to change environments (dev, test, prod)
- Prevents accidental sharing of credentials (since `.env` is usually in `.gitignore`)