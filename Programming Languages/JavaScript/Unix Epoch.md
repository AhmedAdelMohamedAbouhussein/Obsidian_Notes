### 🕒 Unix Epoch (Notes)

- **Definition:**  
    The Unix epoch is the point in time computers use as a starting reference for dates.  
    📍 **1970-01-01 00:00:00 UTC**
    
- **How it works:**
    
    - Time is measured as the number of **seconds** since the epoch.
    - In JavaScript, `Date.now()` gives the number of **milliseconds** since the epoch.
    - `expires_in * 1000` → converts seconds into milliseconds.
        
- **Examples:**
    
    - `0` → 1970-01-01 00:00:00 UTC
    - `1,000,000,000` seconds → 2001-09-09 01:46:40 UTC
    - `1724753100123` ms → current time in 2024
        
- **Why 1970?**  
    Early Unix systems (1960s/70s) needed a baseline, so they picked January 1st, 1970.
    
- **Usage:**
    
    - Token expiration
    - Comparing times
    - Logging & timestamps