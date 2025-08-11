In **Express** (and other web frameworks), **routes** are like a map telling your server:
> “When a request comes to this URL with this HTTP method, run this code.”

They **match an incoming request’s**:
1. **HTTP method** (GET, POST, PUT, DELETE, etc.)
2. **Path** (`/games`, `/games/:gameName`, `/auth/google`, etc.)
and then decide **which function** (controller) to run.

- **Routes**: the _address book_ — they connect URLs to logic.
- **Controllers**: the _workers_ — they contain the actual logic that runs.