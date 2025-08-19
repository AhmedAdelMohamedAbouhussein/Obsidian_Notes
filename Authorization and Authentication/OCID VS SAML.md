## **1. SAML (Security Assertion Markup Language)**

- **Type:** XML-based protocol
- **Main use:** Web browser SSO, especially for enterprise applications
- **How it works:**
    1. User tries to access a Service Provider (SP).
    2. SP redirects user to the Identity Provider (IdP).
    3. IdP authenticates the user and sends back a **SAML Assertion** (XML) via the browser.
    4. SP validates the assertion and logs the user in.
        
- **Token format:** XML
- **Best for:** Enterprise web apps, legacy systems, cross-domain SSO
- **Security:** Uses signed XML assertions and can be encrypted

---

## **2. OIDC (OpenID Connect)**

- **Type:** Modern protocol built on **OAuth 2.0**
- **Main use:** Authentication for web apps, mobile apps, and APIs
- **How it works:**
    1. User authenticates via Identity Provider (IdP).
    2. IdP returns an **ID Token** (JWT - JSON Web Token) and optionally an Access Token.
    3. The client (app) verifies the ID Token and gets user info.
- **Token format:** JSON Web Token (JWT)
- **Best for:** Modern web apps, mobile apps, APIs, and RESTful services
- **Security:** Signed JWTs (usually with JSON Web Key Sets - JWKS)

![[Pasted image 20250819204959.png]]

### **4. When to Use**

- **SAML:** Legacy enterprise apps, corporate intranet, apps requiring XML assertions.
- **OIDC:** New web apps, mobile apps, REST APIs, microservices — easier to integrate with modern stacks.

---

💡 **TL;DR:**

- SAML = Old-school, XML, enterprise web SSO.
- OIDC = Modern, JSON/JWT, works well for web, mobile, and APIs.