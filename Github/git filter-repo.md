### hat is `git filter-repo`?

**`git filter-repo`** is a powerful tool that lets you **rewrite Git history**.

It’s used when you want to:

✅ **Completely remove files or folders** from your Git repository  
✅ **Remove sensitive data** (like passwords, keys) from _all commits_  
✅ **Change commit author info** (e.g., fix wrong names or emails)  
✅ **Split a repo** into multiple smaller repos  
✅ **Clean up large or bloated repos**

### What it _does_

- **Goes through every commit**, branch, and tag in your repo
- **Finds and removes** the file(s), folder(s), or data you specify
- **Rewrites Git history** so it looks like the file was _never there_
- Creates a **new Git history** that you can push to GitHub or other remotes

![[Pasted image 20250806141930.png]]