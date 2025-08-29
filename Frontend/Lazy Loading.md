# What “lazy loading” means (in UI terms)

- **Goal:** Don’t render or fetch heavy stuff (images, big components) **until the user is close to seeing it**.
- **Why:** Faster initial paint, less memory, fewer network requests up front, smoother scrolling.
    
- **How (common patterns):**
    
    1. **Browser image lazy-load**: `<img loading="lazy">` → delays image download.
    2. **Component visibility lazy-render**: Use **IntersectionObserver** to render a component **only when it’s in/near the viewport** (your approach).
    3. **Code splitting**: `React.lazy()` → delays downloading the component **code** until it’s needed.
    4. **List virtualization**: render only visible rows in long lists.
       
# Why this improves performance

- **Less work on first paint:** Cards off-screen render a tiny placeholder instead of full content.
- **Network is staggered:** Images for off-screen cards don’t even exist yet, so they don’t download until needed.
- **Lower memory:** Fewer mounted DOM nodes & components at once.