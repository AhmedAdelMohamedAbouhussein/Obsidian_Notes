## 📘 **JSON (JavaScript Object Notation)**

✅ **Definition:**  
A lightweight data format used for configuration, data exchange, and APIs.

📄 **File extension:** `.json`

📜 **Rules:**

- **Strict syntax**
    
- **No comments allowed**
    
- **Every key must be in double quotes ("")**
    
- **Supports only valid JSON data types:**
    
    - String, Number, Boolean, Null, Object `{}`, Array `[]`
        

📌 **Example (valid JSON):**

`{   "name": "Ahmed",   "age": 21,   "isStudent": true }`

---

## 🗒️ **JSONC (JSON with Comments)**

✅ **Definition:**  
A JSON-like format that **allows comments**, mainly used in **config files** where you want notes or explanations.

📄 **File extension:** `.jsonc`

💡 **Used by:**

- VS Code settings (`settings.jsonc`)
    
- Some tools or editors for readable configs
    

📜 **Extra Features:**

- Supports **single-line comments** (`// ...`)
    
- Supports **multi-line comments** (`/* ... */`)
    
- Otherwise follows normal JSON rules
    

📌 **Example (JSONC):**

`{   // This is Ahmed's profile   "name": "Ahmed",     /* Age and status */   "age": 21,   "isStudent": true }`

---

## ⚖️ **Comparison Summary**

| Feature                  | JSON               | JSONC                             |
| ------------------------ | ------------------ | --------------------------------- |
| File extension           | `.json`            | `.jsonc`                          |
| Comments allowed         | ❌ No               | ✅ Yes (`//` and `/* ... */`)      |
| Used in                  | APIs, data storage | Config files, editors             |
| Readable by JSON parsers | ✅ Yes              | ❌ No (must remove comments first) |
| Strictness               | Very strict        | More flexible for humans          |

---

## 🧠 **In Simple Terms:**

- **JSON** → machine-readable, strict.
- **JSONC** → human-friendly JSON (good for config files, not for APIs).