Here’s a comprehensive list of the **most commonly used Bash shell built-in commands** in Ubuntu/Linux that usually **don’t have their own `man` pages**. You can access their help via `help <command>` instead.

---

### **Navigation / Directory**

- `cd` → Change directory
    
- `pwd` → Print working directory
    
- `pushd` → Save current directory and change to a new one
    
- `popd` → Return to the directory saved by `pushd`
    
- `dirs` → List directories in the stack
    

---

### **Shell Environment / Variables**

- `echo` → Print text or variables
    
- `export` → Set environment variables
    
- `unset` → Remove variables
    
- `set` → Display or set shell options and variables
    
- `readonly` → Mark variables/functions as read-only
    
- `type` → Display information about commands (built-in, external, alias)
    
- `alias` → Create command shortcuts
    
- `unalias` → Remove aliases
    

---

### **Shell Control / Job Management**

- `jobs` → List background jobs
    
- `fg` → Bring job to foreground
    
- `bg` → Send job to background
    
- `wait` → Wait for background jobs to finish
    
- `trap` → Execute a command on signals or events
    
- `exec` → Replace the shell with a command
    

---

### **Functions / Scripts**

- `function` → Define a function
    
- `return` → Return from a function
    
- `break` → Exit a loop
    
- `continue` → Continue to the next iteration of a loop
    

---

### **Conditionals / Shell Options**

- `test` → Evaluate conditional expressions (often `[ ... ]`)
    
- `:` → No-op (does nothing, returns true)
    
- `true` → Always returns true
    
- `false` → Always returns false
    
- `command` → Run a command ignoring shell functions or built-ins
    
- `builtin` → Run a shell built-in command explicitly
    

---

### **Miscellaneous**

- `help` → Show help for built-in commands
    
- `history` → Show shell command history
    
- `exit` → Exit the shell
    
- `times` → Show user and system CPU time