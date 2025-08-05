- <span style="font-size:16px; color:green;">command</span> 
	1. npm install react-router-dom

## 1. `BrowserRouter`

### 📌 What it is:
A component that enables **client-side routing** using the browser's **history API** (without full page reloads).
### 🧠 You use it **once** at the top level of your app. (The **main router container** that allows everything else to work.)
![[Pasted image 20250805122429.png]]

## 2. `Routes`

### 📌 What it is:
A container that holds **all your `<Route />` definitions**.
> Replaces the older `<Switch>` from React Router v5.

(The **routing map** that tells React which component to show based on the URL.)
![[Pasted image 20250805122513.png]]

## 3. `Route`

### 📌 What it is:
Defines a **single route path** and its **corresponding component** (`element`).
![[Pasted image 20250805122625.png]]

## 4. `useNavigate`

### 📌 What it is:
A **hook** that lets you **programmatically navigate** between routes (like `window.location.href`, but SPA-friendly).
(A **JavaScript function to change routes**, usually triggered by an event like button click or login.)
![[Pasted image 20250805122817.png]]

![[Pasted image 20250805122844.png]]