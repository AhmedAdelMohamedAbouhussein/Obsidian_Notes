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

### What kind of database is Redis?

- **In-memory database:** Redis stores data primarily in your server’s RAM, which makes it extremely fast for reads and writes.
- **Key-value store:** It saves data as keys and their associated values, which can be simple strings or complex data types like lists, sets, hashes, and more.
- **Often used as a cache:** Because of its speed, Redis is frequently used to cache data from slower databases or APIs to improve performance.
- **Supports persistence:** While it’s in-memory, Redis can optionally save snapshots to disk to avoid data loss.
- **Versatile:** Besides caching, it’s used for session storage, real-time analytics, leaderboards, queues, and pub/sub messaging.

### So yes, Redis is a database, but it’s specialized for:

- **Speed and low latency** due to in-memory storage
- **Simple key-value operations** and data structures
- **Temporary or fast-access data storage** (though it can be persistent too)