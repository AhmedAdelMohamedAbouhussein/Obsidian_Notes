
---

## 1️⃣ Authentication

Epic uses **OAuth2** for third-party apps:

- **Endpoint:** `https://www.epicgames.com/id/api/authorize`
    
- **Scopes:** `basic_profile` (required), optionally `entitlement:read` or `games` for library info
    
- **Flow:**
    
    1. Redirect user to Epic login page (authorize).
        
    2. User logs in → Epic redirects back to your `redirect_uri` with `code`.
        
    3. Exchange `code` for **access token** at `https://account-public-service-prod03.ol.epicgames.com/account/api/oauth/token`.
        

You will get:

- `access_token` → call Epic APIs
    
- `refresh_token` → to refresh the session
    

---

## 2️⃣ Getting Owned Games

Epic doesn’t officially expose a public “owned games” endpoint, but you can get the **entitlements / purchases** via the **Account Service API**:

- **Endpoint:**
    
    `GET https://account-public-service-prod03.ol.epicgames.com/account/api/public/account/<userId>/entitlements`
    
- **Headers:**
    
    `Authorization: Bearer <access_token>`
    
- **Response:** List of owned games with fields like `namespace`, `offerId`, `titleName`, `devName`, etc.
    

---

## 3️⃣ Achievements / Stats

- Epic doesn’t have a **universal achievements API** like Steam/Xbox.
    
- Achievements are typically **game-specific**, often exposed via the game itself or using **Epic Online Services (EOS)** SDK.
    
- For most web apps, you can at least store **owned games** and the **Epic Account ID**.
    

---

## 4️⃣ Friends List

- Epic has a **Friends API** in EOS.
    
- On web, you can sometimes use:
    
    `GET https://friends-public-service-prod.ol.epicgames.com/friends/api/public/friends/<userId>`
    
- Needs `Authorization: Bearer <access_token>`
    
- Returns basic friend info: display name, Epic ID, avatar.
    

---

## 5️⃣ Data Structure Recommendation

You can store Epic data **similar to Steam/Xbox**:

`{   platform: "Epic",   epicId: "1234567890",   displayName: "GamerTag",   ownedGames: [     {       gameId: "offerId",       gameName: "Fortnite",       devName: "Epic Games",       lastPlayed: null, // optional, not available       achievements: [],       progress: 0     }   ],   friends: [     { externalId, displayName, profileUrl, avatar, status, source: "Epic" }   ] }`

---

## 6️⃣ Suggested Flow

1. **OAuth2 login** → get `access_token` + `refresh_token`.
    
2. **Fetch owned games** → call `/entitlements`.
    
3. **Fetch friends** → call `/friends/api/public/friends/<userId>`.
    
4. **Update your user model** → same as Steam/Xbox flow.
    

This keeps your **backend consistent across all platforms**.