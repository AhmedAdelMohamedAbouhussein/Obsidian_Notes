# Linux Symlinks — Detailed Notes

---

## 1️⃣ Definition

A **symlink (symbolic link)** is a **special type of file** in Linux that points to another file or directory.

- Think of it as a **shortcut** in Windows or macOS
    
- Does **not contain file data** — just a **path to the target**
    
- Changes to the target are reflected when accessing via the symlink
    

---

## 2️⃣ Types of Links in Linux

|Link Type|Description|
|---|---|
|**Hard Link**|Points directly to **inode** of file; multiple names for same file; cannot cross filesystems; cannot link directories|
|**Symbolic Link**|Points to **path** of file; can cross filesystems; can link directories; shows as a pointer|

---

## 3️⃣ Creating Symlinks

### Syntax

	ln -s <target> <link_name>

- `-s` → create **symbolic link**
    
- `<target>` → original file or directory
    
- `<link_name>` → name of symlink to create
    

### Examples

1. File symlink:
    

		ln -s /home/user/file.txt file_link.txt

- Access `file_link.txt` → opens `/home/user/file.txt`
    

2. Directory symlink:
    

		ln -s /var/log mylog

- `mylog` acts as a shortcut to `/var/log`
    

---

## 4️⃣ Viewing Symlinks

- `ls -l` shows symlinks:
    

	lrwxrwxrwx 1 user user 12 Feb 25 12:00 file_link.txt -> /home/user/file.txt

- `file_link.txt -> /home/user/file.txt` indicates **target path**
    

---

## 5️⃣ Removing Symlinks

- Delete like a normal file:
    

		rm file_link.txt

- Only deletes the symlink, **not the target file**
    

---

## 6️⃣ Advantages of Symlinks

- **Shortcut to files/directories**
    
- Can **cross filesystems**
    
- Useful for **versioned files** (e.g., `current -> v1.2`)
    
- **Organize files** without duplicating data
    

---

## 7️⃣ Common Use Cases

1. **Software binaries**:
    

		ln -s /usr/local/bin/node /usr/bin/node

- Allows `node` command system-wide
    

2. **Configuration files**:
    

		ln -s ~/dotfiles/.vimrc ~/.vimrc

- Keep centralized config and symlink to home
    

3. **Version management**:
    

		ln -s python3.10 python

- `python` points to active version
    

---

## 8️⃣ Exam / Interview Points

- **`ln -s target link_name`** → create symlink
    
- **`ls -l`** shows symlink with arrow `->`
    
- Symlink **points to path**, not inode
    
- Can link **files and directories**
    
- **Deleting symlink does not affect target**