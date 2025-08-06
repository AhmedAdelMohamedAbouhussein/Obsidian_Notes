**Redis**  is an **open-source, in-memory data structure store** used as a:

- 🔄 **Cache**
- 📦 **Database**
- 📮 **Message broker**

![[Pasted image 20250806234430.png]]

### Common Use Cases:

- ✅ Caching results (e.g. API responses, DB queries)
- 🔐 Session storage (e.g. user sessions in web apps)
- 📩 Real-time systems (e.g. chat apps, live feeds)
- 📊 Queues and rate-limiting (e.g. background jobs, login throttling)

## What does caching with Redis mean?

Instead of querying a **slow resource** (e.g., database or external API) **every time**, you first:
1. Check if the value exists in Redis.
2. If it exists → Return it (fast 🚀).
3. If it doesn't exist → Query the original source, then save it in Redis for next time.

![[Pasted image 20250806234548.png]]