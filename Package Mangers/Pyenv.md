**What it is:**

- `pyenv` manages multiple Python versions.
    
- Helps avoid conflicts between system Python and project Python.
    

**Key features:**

- Install multiple Python versions.
    
- Switch Python version globally (for all shells) or locally (per project).
    
- Works well with virtual environments.
    

**Basic workflow:**
![[Pasted image 20251212151552.png]]

**How it works:**

- When you call `python`, pyenv intercepts the command and directs it to the correct Python version based on **global/local/project settings**.
    

**Platform support:**

- Linux ✅
    
- macOS ✅
    
- Windows ❌ (requires [pyenv-win](https://github.com/pyenv-win/pyenv-win))