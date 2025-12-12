## 1.**`async` Functions**

- Declared with `async` keyword.
- Always **return a Promise**
- Lets you use `await` inside.
- Example:
![[Pasted image 20250803175822.png]]

## 2. **`await` Keyword**

- Used **inside `async` functions only**.
- Waits for a Promise to **resolve**, **without blocking** other code.
- `await` **pauses only the async function**, not the whole program.
- Makes async code look like sync code.
- Example:
![[Pasted image 20250803175853.png]]