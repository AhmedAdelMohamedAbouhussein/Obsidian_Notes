**CORS (Cross-Origin Resource Sharing)** is a **browser security feature** that **blocks frontend JavaScript code from making requests to a different domain** (or port/protocol) than the one that served the original web page — _unless the other domain explicitly allows it_.

## 🔐 Why does CORS exist?

To protect the user from malicious websites stealing sensitive data using the user’s credentials (cookies, tokens, etc.).

Imagine:
- You're logged into your bank at `https://bank.com`
- Then you visit a malicious website: `https://evil.com`

Without CORS, this site could read your data — **major security issue**.
**CORS prevents this.** Browsers enforce it.


![[Pasted image 20250803181314.png]]
![[Pasted image 20250803181356.png]]

If this header is missing or incorrect, the browser **blocks the response**, and your JavaScript **throws a CORS error** — even if the server returns valid data.



## **Same-Origin Policy (SOP)**

This is the underlying browser rule that:
> “Web pages can only make requests to the same origin.”

An **origin** includes:
- Protocol (http vs https)
- Domain
- Port