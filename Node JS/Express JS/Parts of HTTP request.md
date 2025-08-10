### 🔄 Comparison Table

| Where the data is           | Accessed by  | Example                                 |
| --------------------------- | ------------ | --------------------------------------- |
| URL path (e.g. `/user/:id`) | `req.params` | `/user/42` → `req.params.id = 42`       |
| Query string                | `req.query`  | `/user?id=42` → `req.query.id = 42`     |
| Request body (POST)         | `req.body`   | `body: { id: 42 }` → `req.body.id = 42` |
|                             |              |                                         |
![[Pasted image 20250807232911.png]]

![[Pasted image 20250803182819.png]]