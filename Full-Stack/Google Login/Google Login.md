![[Pasted image 20250807151924.png]]

### What this does:

1. **`useGoogleLogin`**:
    
    - This is a hook provided by the `@react-oauth/google` package.
    - It helps your app interact with Google’s OAuth 2.0 system.
        
2. **`flow: 'auth-code'`**:
    
    - This tells Google to give you an **authorization code** after a successful login (instead of the access token directly).
    - This is more secure — it’s called the **Authorization Code Flow**.
        
3. **`onSuccess: async ({ code }) => { ... }`**:
    
    - When the user successfully logs in, Google gives your app an **authorization code** (a short-lived single-use code).
    - You then send this `code` to your **backend** (`http://localhost:8000/auth/google`).
        
4. **`axios.post(...)`**:
    
    - This makes a POST request to your Node.js backend with the code.
    - Your backend will now use this code to get real **tokens** from Google (access token, refresh token, ID token).

![[Pasted image 20250807152000.png]]
### What each line means:

- `require('dotenv').config();`:
    
    - Loads environment variables from a `.env` file.
    - Example: `CLIENT_ID=your-client-id`, `CLIENT_SECRET=your-secret`
    - You **need this** to keep sensitive keys safe and not hardcoded in your code.
        
- `express.json()`:
    
    - Parses incoming JSON request bodies (like `{ code: '...' }`).
        
- `cors()`:
    
    - Allows your frontend (usually running on `localhost:3000`) to make requests to your backend (`localhost:3001`).
    - Without this, you’ll get CORS errors.

![[Pasted image 20250807152129.png]]
This creates an OAuth2 client using:

- Your **client ID** (public)
- Your **client secret** (private, used **only on server**)
- The redirect URI `'postmessage'` which means the code will be delivered in the body of the HTTP request (suitable for SPA clients).

![[Pasted image 20250807152152.png]]
- `req.body.code`: the authorization code from the frontend
    
- `getToken(code)`: Google exchanges the code for:
    - `access_token`: lets you access user’s Google data
    - `refresh_token`: allows you to get a new access token without logging in again
    - `id_token`: contains basic user info (name, email, etc.)
    
- These are returned to the frontend so you can store or use them.

![[Pasted image 20250807173544.png]]
### **1. `oAuth2Client.setCredentials(tokens);`**

- This sets the `access_token` (and possibly `refresh_token`) **inside the OAuth2 client**.
- Think of it like "logging in" the client with the user's credentials.
- After this, `oAuth2Client` will automatically attach the access token when making requests to Google APIs on behalf of the user.

	![[Pasted image 20250807173729.png]]
- This creates a wrapper for calling **Google’s OAuth2 API**.
- `auth: oAuth2Client` tells it to use the previously authenticated client.
- `version: 'v2'` selects the **v2 API**, which gives access to user info (like email, name, etc.).

### **3. `const userInfoResponse = await oauth2.userinfo.get();`**

- Makes a **GET request** to this Google API endpoint:  
    `https://www.googleapis.com/oauth2/v2/userinfo`
- Returns the user's **profile data** (name, email, picture, etc.).

### **4. `const userInfo = userInfoResponse.data;`**

- Extracts the actual user data from the full API response object.


![[Pasted image 20250807152255.png]]
- If the frontend has a `refresh_token`, it can get a new access token by calling this endpoint.
- Useful when the access token expires (usually after 1 hour).
- You use `UserRefreshClient` from `google-auth-library`.