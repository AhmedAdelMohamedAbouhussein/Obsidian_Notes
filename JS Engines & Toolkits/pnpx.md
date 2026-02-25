## 1️⃣ Definition

**`pnpx`** is a command-line tool that comes with **pnpm**, a fast and efficient **JavaScript package manager**.

- Purpose: **run Node.js binaries from npm packages without installing them globally**
    
- Equivalent to **`npx` (from npm)** but optimized for **pnpm users**
    

---

## 2️⃣ Core Idea

- Normally, to use a CLI from a package, you either:
    
    - Install it **globally**: `npm install -g package`
        
    - Or install locally and use it from `node_modules/.bin/`
        

`pnpx` allows you to **run any package executable directly**, without polluting your global packages:

	pnpx package-name [args]

- Downloads the package if not already present
    
- Runs the binary
    
- Cleans up automatically
    

---

## 3️⃣ Use Cases

1. **One-off commands**: Run a package without global install
    

		pnpx create-react-app my-app

2. **Run a specific version of a package**:
    

		pnpx typescript@4.9 tsc --version

3. **Run binaries from local project dependencies**:
    

pnpx eslint src/

---

## 4️⃣ Comparison: `npx` vs `pnpx`

|Feature|npx (npm)|pnpx (pnpm)|
|---|---|---|
|Package manager|npm|pnpm|
|Installs temporarily|✅|✅|
|Uses pnpm store|❌|✅ (reuses packages efficiently)|
|Speed|Good|Faster for pnpm users|
|Disk space efficiency|Normal|Saves space with pnpm store|

---

## 5️⃣ Example Workflows

### Create a new React project without global install

	pnpx create-react-app my-app

- Downloads `create-react-app` temporarily
    
- Runs it to scaffold project
    
- Removes temporary install after execution
    

---

### Run local dependency

If `eslint` is installed in `devDependencies`:

pnpx eslint src/

- Runs `eslint` from `node_modules/.bin/`
    
- No need for global install
    

---

### Specify package version

pnpx typescript@4.9 tsc --init

- Installs TypeScript 4.9 temporarily
    
- Runs `tsc --init`
    
- Removes temporary install after run
    

---

## 6️⃣ Advantages

- **No global installs** → keeps system clean
    
- **Version control** → can run exact package version
    
- **Faster with pnpm** → uses **pnpm store and hard links**
    
- Works seamlessly with **local project dependencies**
    

---

## 7️⃣ Key Exam / Interview Points

- `pnpx` is like `npx` but for **pnpm users**
    
- Allows **one-time use of CLI tools** without global installs
    
- **Efficient** because it reuses packages in pnpm store
    
- Supports **version specification**