You likely mean **Nodemon** — a helpful tool used during Node.js development.

**Nodemon** is a **dev dependency** that automatically restarts your Node.js application **whenever you make file changes**. It’s used instead of the regular `node` command to improve developer productivity.

- <span style="font-size:16px; color:green;">command</span> 
	1. npm i --save-dev nodemon
### What it does:

- Installs `nodemon` **locally** (inside your project).
- Saves it as a **development dependency** in your `package.json` under `"devDependencies"`, meaning it’s only needed during development—not in production.
![[Pasted image 20250803220430.png]]
- <span style="font-size:16px; color:green;">command</span> 
	2. npm run dev

nodemon VS --watech
![[Pasted image 20250805181456.png]]