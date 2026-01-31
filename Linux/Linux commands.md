## Linux Paths & Directories

- `~` → home directory (e.g. `/home/ahmed`)
    
- `.` → current directory
    
- `..` → previous (parent) directory
    

### Root (`/`) main directories

- `/` → root (top of filesystem)
    
- `/home` → users’ home directories
    
- `/mnt` → mounted disks / temporary mounts
    
- `/var` → variable data (logs, cache, mail, etc.)
    
- `/bin` → essential binary executables (commands like `ls`, `cp`)
    

---

## File Permissions (`ls -l`)

Example:

`-rwxr-xr--`

### Breakdown

`-   rwx   r-x   r-- 
^      ^          ^          ^ 
|         |            |          | 
|       user    group  others 
| 
file type`

### File type

- `-` → file
    
- `d` → directory
    

### Permissions

- `r` → read
    
- `w` → write
    
- `x` → execute
    

---

## Common Commands

### Navigation & Viewing

- `cd` → change directory
    
- `ls` → list directory contents
    
    - `-l` → long description
        
    - `-a` → show hidden files
        
    - `-la` or `-lah` → long + hidden
        
- `pwd` → print working directory
    
- `clear` → clear terminal
    
- `history` → show command history
    

### Files & Editing

- `touch file.txt` → create file / change timestamps
    
- `nano file.txt` → edit file (text editor)
    
- `cat file.txt` → display file content
    
- `echo "text"` → print text
    
- `echo "text" >> file.txt` → append
    
- `>` → overwrite
    
- `>>` → append
    

### File Management

- `rm file` → remove file
    
- `rm -rf dir` → recursive force remove
    
- `cp src dest` → copy
    
- `mv src dest` → move / rename
    
- `mkdir dir` → create directory
    
- `rmdir dir` → remove empty directory
    

### Utilities

- `grep` → search text
    
- `wc` → word/line/byte count
    
- `wget url` → download file
    
- `man command` → manual page
    
- `sudo` → run command as root
    

---

## Pipes & Redirection

- `|` → pipe (output → input)
    

Examples:

`ls | cat >> all.log 
`ls > all.log 
`echo "Ahmed Adel" >> all.log

### Standard Streams

- **stdin** → input
    
- **stdout** → output
    
- **stderr** → error output
    

---

## Batch Operations

`touch f{1..10}.se 
`ls && rm *.se`

---

## Bash & Shell Scripts

- `.sh` → shell script
    
- Bash is a **scripted / interpreted language**
    

### Shebang

`#!/bin/bash`

→ tells Linux which interpreter to use

---

## Permissions (`chmod`)

- `chmod +x file` → make executable
    
- `chmod 777 file` → full access (⚠ not recommended)
    
- `chmod u+x file` → user execute
    
- `chmod g+x file` → group execute
    
- `chmod o+x file` → others execute
    

---

## Running Scripts

`./script.sh     # execute directly 
`bash script.sh  # run with bash`

---

## sudo

- `sudo` = **Super User DO**
    
- Temporarily gives root permissions

---

## Programming Analogy

`add(x, y);            // arguments 
`add(int x, int y);    // parameters`

---

## Assignment Hint (File deletes after 1 hour)

`touch temp.txt 
`sleep 3600 && rm temp.txt`