## 1. Callbacks

- A **callback** is a function passed as an argument to another function and is called after an operation completes.
-  Problems with callbacks:: **Callback hell** (nested callbacks make code hard to read):
- **Error handling is messy**: need to manually check for errors.
- Harder to debug and maintain.
- Example:
![[Pasted image 20250803180228.png]]
## 2. Promises

A **Promise** represents a future value. It has 3 states:
- `pending` (not finished)
- `fulfilled` (done successfully)
- `rejected` (failed)
- Example:
![[Pasted image 20250803180425.png]]

### ✅ Benefits of Promises:

- Clean, **chainable** syntax using `.then()` and `.catch()`
- Works smoothly with `async/await`
- Better **error handling**

![[Pasted image 20250803180516.png]]