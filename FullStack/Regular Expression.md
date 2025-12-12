A **regular expression** (regex) is a sequence of characters that defines a **search pattern**. It is mainly used for **matching, searching, and manipulating text** in programming, scripting, and text-processing tasks.

**Key Features:**

1. **Pattern Matching:**  
    Regex describes a pattern to identify strings. For example, the pattern `cat` matches the word `"cat"` in `"concatenate"` depending on context.
    
2. **Special Characters (Metacharacters):**
    
    - `.` → Matches any single character except a newline.
        
    - `*` → Matches 0 or more occurrences of the preceding element.
        
    - `+` → Matches 1 or more occurrences of the preceding element.
        
    - `?` → Matches 0 or 1 occurrence of the preceding element.
        
    - `^` → Matches the start of a line.
        
    - `$` → Matches the end of a line.
        
    - `[abc]` → Matches any one character within the brackets (a, b, or c).
        
    - `[^abc]` → Matches any character except a, b, or c.
        
    - `(pattern)` → Groups multiple characters or expressions.
        
    - `|` → Acts as OR between patterns.
        
3. **Escaping Special Characters:**  
    To match a special character literally, use `\`. For example, `\.` matches a literal period.
    
4. **Common Uses:**
    
    - Validating input formats such as emails, phone numbers, or passwords.
    - Searching or extracting text in tools like `grep`, `sed`, or `awk`.
    - Replacing or modifying strings in programming languages.