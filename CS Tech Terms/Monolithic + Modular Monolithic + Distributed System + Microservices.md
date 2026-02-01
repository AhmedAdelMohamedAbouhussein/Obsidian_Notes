## 1️⃣ Monolithic

**Definition:**  
Everything (UI, business logic, database access) in **one codebase and deployment unit**.

**Architecture:**

![[Pasted image 20260201211824.png]]

**Pros:** Simple, easy to build and deploy  
**Cons:** Hard to scale, tightly coupled, one bug can crash everything  
**Use cases:** Small apps, MVPs, solo projects

---

## 2️⃣ Modular Monolithic

**Definition:**  
Still one deployment, but **code is divided into modules** (Auth, Payment, Orders, etc.) for better maintainability.

**Architecture:**

![[Pasted image 20260201211835.png]]

**Pros:** Easier to maintain, better code organization, still simple to deploy  
**Cons:** Scaling still “all or nothing”  
**Use cases:** Medium-sized apps, growing teams

---

## 3️⃣ Distributed System

**Definition:**  
App split into **independent services**, communicating over a network. Can be multiple microservices or other distributed architectures.

**Architecture (general):**

![[Pasted image 20260201211847.png]]

**Pros:** Scalable, fault-tolerant, teams work independently  
**Cons:** Complex deployment, network overhead, requires DevOps expertise  
**Use cases:** Large-scale apps, high traffic systems

---

## 4️⃣ Microservices (a type of distributed system)

**Definition:**  
Each service handles a **single business capability**, is **loosely coupled**, and deploys independently.

**Architecture (example):**

![[Pasted image 20260201211859.png]]

**Pros:** Independent scaling & deployment, fault isolation, polyglot-friendly  
**Cons:** Network latency, distributed transactions, complex monitoring & testing  
**Use cases:** Netflix, Amazon, Spotify, Uber, large enterprise apps

---

### Comparison Table

| Feature              | Monolithic      | Modular Monolithic | Distributed (general) | Microservices (specific)    |
| -------------------- | --------------- | ------------------ | --------------------- | --------------------------- |
| **Codebase**         | Single          | Single, modular    | Multiple independent  | Multiple independent        |
| **Deployment**       | Single unit     | Single unit        | Multiple units        | Multiple units              |
| **Scaling**          | Whole app       | Whole app          | Per service           | Per service                 |
| **Fault isolation**  | Poor            | Medium             | Good                  | Excellent                   |
| **Team size**        | Small           | Medium             | Medium-Large          | Large                       |
| **Complexity**       | Low             | Medium             | High                  | Very High                   |
| **Network overhead** | None            | Minimal            | High                  | High                        |
| **Tech flexibility** | Low             | Medium             | High                  | High                        |
| **When to use**      | Small apps, MVP | Growing apps       | Large apps, scalable  | Large, enterprise, scalable |

---

💡 **Pro tip:**  
Most systems **evolve gradually**:  
**Monolithic → Modular Monolithic → Distributed → Microservices**

This is how startups usually grow their architecture.