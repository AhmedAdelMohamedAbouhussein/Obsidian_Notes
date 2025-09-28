`nanoid` is a **JavaScript library** for generating unique, random, and URL-friendly IDs. It’s widely used as an alternative to UUIDs because it produces shorter strings while still being highly unique.

### Key points about `nanoid`:

- **Length**: By default, it generates a 21-character string (but you can choose the length).
    
- **Characters used**: Uses `A-Z`, `a-z`, `0-9`, `-`, and `_` (URL-safe).
    
- **Uniqueness**: The chance of collision is extremely low (similar or even better than UUID v4 for practical use).
    
- **Performance**: Faster than most UUID libraries because it’s optimized for speed.
    
- **Use case**: Perfect for generating public IDs, short links, or user-facing identifiers where `_id` (Mongo ObjectId) would be too sensitive or ugly.
![[Pasted image 20250928224105.png]]

