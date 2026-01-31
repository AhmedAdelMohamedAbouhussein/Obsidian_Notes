# Diffing

### Meaning

**Diffing** = the process of **comparing two sets of data or files** to identify **differences**.

- Common in software development, version control, and text comparison.

---

### 1. Diffing in Programming / Version Control

- Used to **see what changed** between:
    
    - Two versions of a file
    - Two commits in Git
    - Two branches or releases
        
- Highlights:
    
    - Lines added
    - Lines removed
    - Lines modified
        

**Example (Git):**

`git diff commit1 commit2`

- Shows line-by-line differences between two commits    

---

### 2. How Diffing Works

- Compares **content line by line** (or sometimes word/character level)    
- Marks:
    - `+` → line added
    - `-` → line removed

- Algorithms used: **Longest Common Subsequence (LCS)**, Myers diff algorithm
    

---

### 3. Use Cases

1. **Code reviews**
    
    - Understand changes before merging
        
2. **Debugging**
    
    - Compare expected vs actual outputs
        
3. **Version control**
    
    - Track history of changes
        
4. **Document comparison**
    
    - Detect edits in text files
        

---

### 4. Memory Hook

- Think: **“diff = difference”**
    
- Diffing tells you **what changed**.
    

---

### 5. One-Line Exam Answer

> Diffing is the process of comparing two files or datasets to identify additions, deletions, or modifications, commonly used in version control and code review.