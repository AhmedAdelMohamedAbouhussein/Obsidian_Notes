## 1️⃣ Definition

**pnpm** is a **fast, disk-efficient JavaScript package manager**.

- Alternative to **npm** and **Yarn**
    
- Focuses on **speed, efficiency, and reliability**
    
- Uses a **content-addressable storage (CAS)** to **store only one copy of each package version** on your machine, even across multiple projects
    

---

## 2️⃣ Key Features

|Feature|Description|
|---|---|
|Disk efficiency|Uses **symlinks** to share packages between projects|
|Fast installs|No redundant downloads|
|Strict dependency tree|Avoids “phantom dependencies” that can happen in npm/Yarn|
|Compatibility|Supports **npm registry packages**, works like npm|
|CLI commands|Same commands as npm: `pnpm install`, `pnpm add`, `pnpm remove`|
|Works with workspaces|Great for **monorepos**|

---

## 3️⃣ How pnpm Works

1. Packages are **downloaded once** to a **global store** on your machine
    
2. Projects create **symlinks** from `node_modules` to the global store
    
3. Only dependencies explicitly listed in `package.json` are available — prevents accidental dependency usage
    
4. Supports **strict mode**: enforces dependency graph
    

---

## 4️⃣ Comparison with npm and Yarn

|Feature|npm|Yarn|pnpm|
|---|---|---|---|
|Disk usage|High|Medium|Low (symlinked)|
|Speed|Moderate|Fast|Very fast|
|Strict dependency tree|No|Partial|Yes|
|Monorepo support|Moderate|Yes|Excellent|
|Node_modules structure|Flat|Flat|Nested symlinks|

---

## 5️⃣ Installation

# Using npm  
npm install -g pnpm  
  
# Check version  
pnpm --version

---

## 6️⃣ Common Commands

|Command|Description|
|---|---|
|`pnpm install`|Install dependencies from `package.json`|
|`pnpm add <package>`|Add a dependency to the project|
|`pnpm remove <package>`|Remove a dependency|
|`pnpm update`|Update dependencies|
|`pnpm exec <command>`|Run a command in the project context (like npx)|
|`pnpm list`|List installed dependencies|
|`pnpm store status`|Show global store usage|
|`pnpm add -D <package>`|Add a dev dependency|

---

## 7️⃣ Example Usage

### Create a new project

mkdir my-app  
cd my-app  
pnpm init  
pnpm add react react-dom

- Dependencies are stored in **pnpm global store**
    
- `node_modules` contains **symlinks**, saving space
    

### Run a CLI package once

pnpx create-react-app my-app

- Runs the package temporarily without global install
    

---

## 8️⃣ Advantages

- **Disk efficient** → saves space with symlinks
    
- **Faster installs** → avoids repeated downloads
    
- **Strict and predictable dependency graph** → avoids hidden bugs
    
- **Works well for monorepos** → better than npm/Yarn in large projects
    

---

## 9️⃣ Limitations

- Smaller community than npm or Yarn
    
- Some old tools assume **flat `node_modules`** → may need adaptation
    
- Symlinked modules may cause issues in **some OS setups or tools**
    

---

## 🔟 Key Exam / Interview Points

- **pnpm = package manager like npm/Yarn**, but **faster and disk-efficient**
    
- Uses **global store + symlinks** → avoids multiple copies
    
- Compatible with **npm packages**, can replace npm commands
    
- Works well with **workspaces and monorepos**