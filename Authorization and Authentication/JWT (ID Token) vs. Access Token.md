![[Pasted image 20250805143141.png]]

### 🧠 So what does the access token have that the JWT doesn’t?

➡️ **Power to access protected resources**  
The **access token** doesn’t usually _contain_ more info — instead, it acts as a **key** to access Google services **on behalf of the user**.

- The **ID token** is for _your frontend/backend_ to know who the user is.
- The **access token** is for _Google APIs_ to verify if this app is allowed to fetch data for that user.
    
 Think of it like:
> - D token** = passport showing who the user is.
> - **Access token** = entry ticket allowing you to get into certain buildings (APIs).

![[Pasted image 20250805143237.png]]