## **1️⃣ Route Parameters (useParams)**

- **Defined in the route path** with a `:` prefix.
- Are part of the URL **path** itself.
- Extracted in React Router using `useParams()`.
- Example:
![[Pasted image 20250811190212.png]]
Typically used for **identifiers** (IDs, names, slugs) that define a _specific resource_.

## **2️⃣ Query Parameters (search params)**

- Appear **after** a `?` in the URL, separated by `&` if multiple.
- Not defined in the route path.
- Extracted in React Router using `useSearchParams()` or `window.location.search`.
- Example:
![[Pasted image 20250811190334.png]]Typically used for **filters, searches, and sorting** because they’re optional and can be combined.

![[Pasted image 20250811190400.png]]

If you’re building your game pages,
- **`/games/:gameName`** is perfect for unique game detail pages.
- **`/games?search=...`** is better for search results or filtered lists.