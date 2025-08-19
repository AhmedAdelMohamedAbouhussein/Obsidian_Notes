**SAML** (Security Assertion Markup Language) is an **open standard for Single Sign-On (SSO)**. It lets users log in to multiple applications using a **single set of credentials**, often used in enterprise environments. Here’s a clear breakdown:

## **1. What SAML is**

- XML-based protocol for exchanging **authentication and authorization data** between:
    
    1. **Identity Provider (IdP)** – the system that verifies the user (e.g., Okta, Azure AD, Google Workspace).
    2. **Service Provider (SP)** – the application or website the user wants to access (e.g., Salesforce, Jira).
        
- SAML allows the SP to **trust the IdP** without storing passwords itself.

## **2. How SAML Works (Simplified Flow)**

1. User tries to access a service (SP).
2. SP detects the user is not logged in and redirects them to the IdP.
3. User authenticates at the IdP (username/password, MFA, etc.).
4. IdP generates a **SAML Assertion** (an XML document) containing:
    - User identity
    - Attributes/roles
    - Expiration info
5. Assertion is sent back to the SP (usually via browser redirect).
6. SP validates the assertion (signature check) and logs the user in.
![[Pasted image 20250819204824.png]]

## **3. Key Components**

- **Assertion** – The XML document with user info and authentication result.
- **Protocol** – How SP and IdP communicate (usually HTTP Redirect, POST, or Artifact binding).
- **Bindings** – Rules for sending assertions (HTTP POST, HTTP Redirect, SOAP).
- **Profiles** – Specific use cases (e.g., Web Browser SSO).

---

## **4. Advantages of SAML**

- Centralized authentication (SSO)
- No need for SP to store passwords
- Works across domains and applications
- Secure (uses digital signatures and encryption)

---

## **5. Common Use Cases**

- Enterprise Single Sign-On for employees
- Cloud apps like Salesforce, Slack, Google Workspace, Microsoft 365
- Connecting multiple apps under one authentication provider