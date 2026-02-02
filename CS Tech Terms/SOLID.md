SOLID is a set of **5 object-oriented design principles**

## **SOLID Principles**

### **S — Single Responsibility Principle (SRP)**

> A class should have **only one reason to change**.

- Each class should do **one job**.
    
- Avoid “god classes”.
    

**Example:**  
❌ A `User` class that handles user data **and** saves to the database  
✅ `User` + `UserRepository`

---

### **O — Open/Closed Principle (OCP)**

> Software entities should be **open for extension**, but **closed for modification**.

- Add new behavior **without changing existing code**
    
- Use **inheritance** or **interfaces**
    

**Example:**  
Add new payment methods by creating new classes, not editing old ones.

---

### **L — Liskov Substitution Principle (LSP)**

> Subclasses must be usable **where their parent class is expected**.

- Child classes should not break parent behavior
    
- No unexpected exceptions or behavior changes
    

**Example:**  
If `Bird` has `fly()`, then `Penguin` should NOT extend `Bird`.

---

### **I — Interface Segregation Principle (ISP)**

> Many **small interfaces** are better than one **large interface**.

- Don’t force classes to implement methods they don’t need
    

**Example:**  
❌ `Machine` with `print()`, `scan()`, `fax()`  
✅ `Printer`, `Scanner`, `Fax` interfaces

---

### **D — Dependency Inversion Principle (DIP)**

> Depend on **abstractions**, not concrete implementations.

- High-level modules shouldn’t depend on low-level modules
    
- Use **interfaces** instead of concrete classes
    

**Example:**  
`Service` depends on `Database` interface, not `MySQLDatabase`

---

## **Why SOLID Matters**

- Easier to **maintain**
    
- Easier to **test**
    
- Easier to **extend**
    
- Fewer bugs when requirements change
    

---

## **One-line Summary (great for exams)**

> **SOLID** is a set of design principles that improves **code quality, flexibility, and maintainability** in object-oriented software.