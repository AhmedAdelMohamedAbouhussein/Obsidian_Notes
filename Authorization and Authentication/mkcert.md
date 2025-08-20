## 🔹 What is `mkcert`?

- `mkcert` is a simple tool that creates **locally trusted SSL/TLS certificates**.
    
- Normally, when you try to run your app with `https://localhost`, your browser shows a **"Not Secure" / certificate warning**, because the certificate isn’t signed by a trusted Certificate Authority (CA).
    
- `mkcert` solves this by creating your own **local CA** and adding it to your computer/browser as a trusted authority. Then it issues certificates for `localhost` (or any domain you want).

So instead of using self-signed certs that browsers reject, `mkcert` makes certificates that your machine trusts immediately.

---

## 🔹 How it Works

1. **Install mkcert** on your machine.
    
2. Run `mkcert -install` → this creates and installs a **local Certificate Authority** (trusted only on your machine).
    
3. Run `mkcert localhost 127.0.0.1 ::1` → this generates `localhost.pem` and `localhost-key.pem`.
    
4. Configure your backend (Node.js, Express, etc.) to use these certs with HTTPS.

Example in Express:
![[Pasted image 20250820234050.png]]