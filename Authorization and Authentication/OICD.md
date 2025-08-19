OIDC = **OpenID Connect** ✅

It’s an **identity layer built on top of OAuth 2.0**.

- OAuth 2.0 mainly handles **authorization** (granting apps access to resources on behalf of a user).
- OIDC adds **authentication** (verifying who the user is).

### Key Points:

- Uses **JSON Web Tokens (JWTs)** for securely sharing identity information.
- Provides a standardized way for apps to **log users in** without managing passwords themselves.
- Widely used in **Single Sign-On (SSO)** systems.

### Example flow:

1. Your app redirects the user to a provider (Google, Microsoft, etc.).
2. The provider authenticates the user.
3. The provider sends back an **ID token (JWT)** + **access token**.
4. Your app uses the ID token to know **who the user is**, and the access token for API access.
    
👉 In short:
- **OAuth 2.0 = “Can this app access my data?”**
- **OIDC = “Who is this user?”**