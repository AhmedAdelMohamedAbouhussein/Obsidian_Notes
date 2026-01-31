# ACID Properties

**ACID** is a set of properties that guarantee **reliable database transactions**.

A **transaction** is a group of operations that must be treated as **one unit of work**.

ACID ensures:

> Correctness, consistency, and safety of data — even with crashes or concurrent users.

---

## A — Atomicity

### Meaning

A transaction is **all or nothing**.

### What Happens
- Either **all operations succeed**
- Or **none of them are applied**

### Example

Bank transfer:
- Deduct $100 from Account A
- Add $100 to Account B

If the system crashes after deduction but before addition → **rollback**.

### Key Mechanism

- Rollback
- Undo logs

---

## C — Consistency

### Meaning

A transaction takes the database from **one valid state to another valid state**.

### What Is Enforced

- Constraints (primary key, foreign key)
- Rules (balance ≥ 0)
- Triggers

### Example

- Balance cannot become negative
- Foreign key must reference an existing row

If a transaction violates rules → **rejected**.

---

## I — Isolation

### Meaning

Concurrent transactions **do not interfere** with each other.

Each transaction behaves **as if it were running alone**.

### Problems Prevented

- Dirty reads
- Non-repeatable reads
- Phantom reads

### Isolation Levels

- Read Uncommitted
- Read Committed
- Repeatable Read
- Serializable (strongest)

### Example

Two users booking the last seat:

- Isolation prevents both from booking it.

---

## D — Durability

### Meaning

Once a transaction is **committed**, it stays committed.

Even if:
- Power loss
- Crash
- Restart

### How It’s Achieved

- Write-ahead logging
- Disk persistence
- Replication

---

## ACID Summary Table

|Property|Guarantees|
|---|---|
|Atomicity|All or nothing|
|Consistency|Valid state only|
|Isolation|No interference|
|Durability|Data survives crashes|

---

## ACID in Real Databases

Used by:

- MySQL (InnoDB)
- PostgreSQL
- Oracle
- SQL Server

Perfect for:

- Banking systems
- Financial apps
- Inventory systems
- Reservation systems

---

## ACID vs BASE (Quick Contrast)

|ACID|BASE|
|---|---|
|Strong consistency|Eventual consistency|
|Strict transactions|High availability|
|Slower|Faster|
|SQL databases|NoSQL databases|

---

## One-Paragraph Exam Answer

> ACID is a set of properties that ensure reliable database transactions. Atomicity ensures that a transaction is all or nothing, Consistency ensures that database rules are maintained, Isolation prevents concurrent transactions from interfering, and Durability guarantees that committed data persists even after system failures