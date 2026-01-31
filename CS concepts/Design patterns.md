## 1. Introduction to Design Patterns

**Design Patterns** are **reusable solutions** to common problems that occur frequently in software design.  
They are **not code**, but **templates or best practices** that guide how to structure classes and objects.

Key goals:

- Improve **code reusability**
- Increase **maintainability**
- Reduce **tight coupling**
- Make systems **scalable and flexible**

Design patterns were popularized by the **Gang of Four (GoF)**.

---

## 2. Classification of Design Patterns

Design patterns are generally divided into **three main types**:

1. **Creational Patterns**
2. **Structural Patterns**
3. **Behavioral Patterns**

---

# 3. Creational Design Patterns

Creational patterns focus on **object creation mechanisms**, ensuring objects are created in a controlled and flexible way.

### Purpose:

- Hide object creation logic
- Improve flexibility
- Reduce dependency on concrete classes

---

## 3.1 Singleton Pattern

### Definition:

Ensures a class has **only one instance** and provides a **global access point**.

### Use Cases:

- Database connections
- Configuration managers
- Logging systems

### Advantages:

- Controlled access to a single instance
- Saves resources

### Disadvantages:

- Can cause hidden dependencies
- Harder to test

![[Pasted image 20251218143628.png]]

---

## 3.2 Factory Method Pattern

### Definition:

Defines an interface for creating objects but lets subclasses decide **which class to instantiate**.

### Use Cases:

- UI components
- Object creation based on input type

### Advantages:

- Loose coupling
- Easy to extend

![[Pasted image 20251218143658.png]]

---

## 3.3 Abstract Factory Pattern

### Definition:

Provides an interface for creating **families of related objects** without specifying their concrete classes.

### Use Cases:

- Cross-platform UI toolkits
- Theme systems (dark/light)

### Difference from Factory Method:

- Factory Method → creates **one object**
- Abstract Factory → creates **groups of objects**

![[Pasted image 20251218143730.png]]

---

## 3.4 Builder Pattern

### Definition:

Separates the construction of a complex object from its representation.

### Use Cases:

- Creating complex objects step-by-step
- Immutable objects
    

### Advantages:

- Clear construction process
- Improves readability

![[Pasted image 20251218143840.png]]
![[Pasted image 20251218143852.png]]

---

## 3.5 Prototype Pattern

### Definition:

Creates new objects by **cloning existing ones**.

### Use Cases:

- Game development
- Expensive object creation

![[Pasted image 20251218143956.png]]

---

# 4. Structural Design Patterns

Structural patterns deal with **how classes and objects are composed** to form larger structures.

### Purpose:

- Simplify relationships
- Improve flexibility
- Reduce complexity

---

## 4.1 Adapter Pattern

### Definition:

Allows incompatible interfaces to work together.

### Use Cases:

- Integrating legacy systems
- Third-party libraries

### Example:

Power plug adapter

![[Pasted image 20251218144200.png]]

---

## 4.2 Bridge Pattern

### Definition:

Separates abstraction from implementation so they can evolve independently.

### Use Cases:

- Graphics systems
- Device drivers

![[Pasted image 20251218144356.png]]

---

## 4.3 Composite Pattern

### Definition:

Treats individual objects and compositions of objects **uniformly**.

### Use Cases:

- File systems
- GUI components

![[Pasted image 20251218144526.png]]

---

## 4.4 Decorator Pattern

### Definition:

Adds behavior to objects **dynamically** without modifying their class.

### Use Cases:

- Adding features at runtime
- Java I/O streams

### Advantage:

- Avoids class explosion

![[Pasted image 20251218144646.png]]

---

## 4.5 Facade Pattern

### Definition:

Provides a **simplified interface** to a complex subsystem.

### Use Cases:

- APIs
- Libraries


![[Pasted image 20251218144831.png]]

---

## 4.6 Proxy Pattern

### Definition:

Provides a placeholder or surrogate to control access to another object.

### Use Cases:

- Lazy loading
- Security
- Remote objects

![[Pasted image 20251218144845.png]]

---

# 5. Behavioral Design Patterns

Behavioral patterns focus on **communication between objects** and **responsibility distribution**.

---

## 5.1 Observer Pattern

### Definition:

Defines a one-to-many dependency so that when one object changes state, all dependents are notified.

### Use Cases:

- Event systems
- GUI listeners

![[Pasted image 20251218150109.png]]

---

## 5.2 Strategy Pattern

### Definition:

Defines a family of algorithms and makes them interchangeable.

### Use Cases:

- Sorting algorithms
- Payment methods

![[Pasted image 20251218150335.png]]

---

## 5.3 Command Pattern

### Definition:

Encapsulates a request as an object.

### Use Cases:

- Undo/Redo
- GUI buttons

![[Pasted image 20251218150832.png]]

---

## 5.4 State Pattern

### Definition:

Allows an object to change behavior when its internal state changes.

### Use Cases:

- Game characters
- Workflow systems

![[Pasted image 20251218150848.png]]

---

## 5.5 Chain of Responsibility Pattern

### Definition:

Passes a request along a chain of handlers.

### Use Cases:

- Event handling
- Logging frameworks

![[Pasted image 20251218151048.png]]

---

## 5.6 Template Method Pattern

### Definition:

Defines the skeleton of an algorithm while allowing subclasses to redefine steps.

### Use Cases:

- Framework design

![[Pasted image 20251218151211.png]]

---

## 5.7 Mediator Pattern

### Definition:

Reduces communication complexity by introducing a mediator object.

### Use Cases:

- Chat systems
- UI coordination

![[Pasted image 20251218151246.png]]

---

## 6. Comparison Table (Quick Revision)

|Category|Focus|
|---|---|
|Creational|Object creation|
|Structural|Object composition|
|Behavioral|Object interaction|

---

## 7. Benefits of Using Design Patterns

✔ Improves code quality  
✔ Encourages best practices  
✔ Makes systems easier to maintain  
✔ Common vocabulary among developers

---

## 8. Summary

Design patterns provide **proven solutions** to recurring design problems.  
Understanding them helps you:

- Design better software
- Write cleaner code
- Think like a software architect