**BFG Repo-Cleaner** is a fast tool used to **remove sensitive data** or **large files** from a Git repository’s entire history — not just the current commit.

Think of it like `git filter-branch` but **100x faster and easier**.

### 🔧 What It’s Used For:

- Deleting large files from the entire history (e.g. `node_modules`, `.env`, `secret_keys.json`)
- Removing accidentally committed passwords or API keys
- Shrinking huge Git repositories

### How to Use BFG

![[Pasted image 20250805154845.png]]

![[Pasted image 20250805154902.png]]

### ⚠️ WARNING

- You are rewriting history. All collaborators need to re-clone the repo.
- Make a **backup** of your repo before doing this.