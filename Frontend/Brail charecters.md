Braille characters are patterns of **raised dots** used by visually impaired people to read and write. Each Braille cell is made up of **6 dots** arranged in **two columns of three** like this:
![[Pasted image 20251018002001.png]]
By raising different combinations of these dots, you get different **letters, numbers, and symbols**.


### 💡 In Web Development

Braille-like characters (⠁⠃⠇⠋ etc.) are **Unicode symbols** from the **Braille Patterns block (U+2800 to U+28FF)**.

Developers sometimes use them **not for real Braille**, but for **loading animations**, **spinners**, or **text effects**, because they look cool and minimal — like moving dots.

---

### ⚙️ Example: Loading Spinner Using Braille Characters
![[Pasted image 20251018002142.png]]

### 🌀 How It Works

- The array `frames` contains **Braille spinner characters**.
    
- `setInterval()` changes the character every `100ms`.
    
- This creates a smooth **text-based loading animation** — just like in CLI tools or terminals.
    

---

### 🧩 Common Braille Spinner Frames

These are the 10 Unicode characters usually used for “loading”:

`⠋ ⠙ ⠹ ⠸ ⠼ ⠴ ⠦ ⠧ ⠇ ⠏`
