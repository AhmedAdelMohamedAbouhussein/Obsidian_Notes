## 1️⃣ Definition

**Yarn** is a **JavaScript package manager** developed by Facebook (Meta) to address some of npm’s shortcomings.

- Manages dependencies for **Node.js projects**
    
- Focuses on **speed, determinism, and reliability**
    
- Uses a **lockfile (`yarn.lock`)** to ensure consistent installs across machines
    

---

## 2️⃣ Key Features

|Feature|Description|
|---|---|
|Fast installation|Uses **parallel downloads** of packages|
|Deterministic installs|`yarn.lock` ensures **exact same dependency tree**|
|Offline mode|Can install from **cache** if package already downloaded|
|Workspaces|Supports **monorepos** with multiple packages|
|Security|Checks package integrity via **checksums**|
|Compatibility|Works with **npm registry packages**|

---

## 3️⃣ Yarn vs npm

|Feature|npm|Yarn|
|---|---|---|
|Speed|Moderate|Fast (parallel)|
|Lockfile|package-lock.json|yarn.lock|
|Offline installation|Limited|Yes|
|Deterministic dependency tree|Partial|Yes|
|Monorepo support|Basic|Excellent|
|CLI commands|npm|yarn (similar)|

---

## 4️⃣ Yarn Versions

- **Yarn Classic (v1)** → original, widely used
    
- **Yarn v2 / Berry** → modern rewrite with **plug’n’play (PnP)** and improved performance
    
- PnP replaces `node_modules` with a **virtual file system**, avoiding traditional folder installs
    

---

## 5️⃣ Installation

# Using npm  
npm install -g yarn  
  
# Check version  
yarn --version

---

## 6️⃣ Common Commands

|Command|Description|
|---|---|
|`yarn init`|Initialize a new project|
|`yarn add <package>`|Add a dependency|
|`yarn add <package> --dev`|Add dev dependency|
|`yarn remove <package>`|Remove a dependency|
|`yarn install`|Install dependencies from `package.json` and `yarn.lock`|
|`yarn upgrade <package>`|Update a dependency|
|`yarn list`|List installed packages|
|`yarn workspaces`|Manage monorepo packages|

---

## 7️⃣ Example Usage

### Create a new project

mkdir my-app  
cd my-app  
yarn init -y       # initialize project  
yarn add react react-dom   # add dependencies  
yarn install       # install all dependencies

- Creates a **`node_modules` folder**
    
- Generates a **`yarn.lock` file** for reproducibility
    

---

### Add a dev dependency

yarn add -D typescript

- Adds `typescript` as a **dev dependency**
    
- Updates `yarn.lock`
    

---

## 8️⃣ Workspaces (Monorepos)

- Define multiple packages in one repo
    
- Example `package.json`:
    

{  
  "private": true,  
  "workspaces": ["packages/*"]  
}

- Automatically links packages internally → no need to publish to npm
    

---

## 9️⃣ Advantages

- Faster installs (**parallel downloads**)
    
- Deterministic installs with **lockfile**
    
- Offline mode for repeated installs
    
- Excellent **monorepo support**
    
- Compatible with **npm registry packages**
    

---

## 🔟 Limitations

- Larger learning curve than npm for beginners
    
- Yarn v2+ PnP may **break old Node.js tools** expecting `node_modules`
    
- Extra tooling required for full **Berry features**
    

---

## 1️⃣1️⃣ Key Exam / Interview Points

- Yarn = **fast, deterministic npm alternative**
    
- Uses **`yarn.lock`** for exact versions
    
- Supports **workspaces** for monorepos
    
- Commands are similar to npm but often **faster and more reliable**