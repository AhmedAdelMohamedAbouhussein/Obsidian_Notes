### **What Are Client ID and Client Secret?**

When you use **OAuth 2.0** to let users log in using a third-party provider (like Google), your app must **identify itself** to Google's servers. That’s what the **Client ID** and **Client Secret** are used for.

They are **credentials for your app**, not for the user.

### **Client ID**

- **Purpose**: Public identifier of your app.
- **Who sees it**: It's okay if users see it (e.g., in frontend code).
- **What it tells Google**: “Hey, I’m App X – can I start a login flow for this user?”

### **Client Secret**

- **Purpose**: Private password for your app.
- **Who should see it**: Only your **backend server**. Never expose it to the frontend.
- **What it tells Google**: “I’m App X, and I can prove it – here’s my secret.”

![[Pasted image 20250807152722.png]]