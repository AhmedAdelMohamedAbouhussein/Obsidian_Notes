### **Object-Oriented Programming (OOP)**

**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of **objects**.  
An object is a combination of **data (attributes)** and **functions (methods)** that work together to represent real-world entities.

The main idea behind OOP is to **organize code** in a way that models how we think about the world — as a collection of objects that interact with each other.  
This makes programs **more modular, reusable, and easier to maintain**.

---

### **Core Concepts of OOP**

1. ### **Class**
    
    A **class** is a **blueprint or template** for creating objects.  
    It defines the **properties (attributes)** and **behaviors (methods)** that the objects will have.
    
    🧩 _Example (in Python):_
    ![[Pasted image 20251018013534.png]]
    
    
2. ### **Object**
    
    An **object** is an **instance of a class**.  
    It represents a specific example created from that class template.
    
    🧩 _Example:_
    ![[Pasted image 20251018013543.png]]
    
    
3. ### **Encapsulation**
    
    **Encapsulation** means **hiding the internal details** of an object and only exposing what’s necessary.  
    This protects the data and prevents it from being modified directly.
    
    🧠 Think of it like a “protective shell” around the object’s data.  
    In Python, this can be done using private variables (by prefixing with `_` or `__`).
    ![[Pasted image 20251018013559.png]]
    
    
4. ### **Abstraction**
    
    **Abstraction** means **showing only the essential features** and hiding the complex implementation details.  
    It simplifies how we interact with objects.
    
    🧠 Example: When you drive a car, you don’t need to know how the engine works — just how to use the steering wheel and pedals.
    ![[Pasted image 20251018013614.png]]
    
    
5. ### **Inheritance**
    
    **Inheritance** allows a class to **inherit properties and behaviors** from another class.  
    This promotes **code reusability** and helps create hierarchical relationships.
    ![[Pasted image 20251018013622.png]]
    
    
6. ### **Polymorphism**
    
    **Polymorphism** means **“many forms.”**  
    It allows different classes to have methods with the same name but different behaviors.  
    This makes code more flexible and easier to extend.
    ![[Pasted image 20251018013630.png]]
    
    

---

### **Advantages of OOP**

- **Reusability** – Code can be reused through inheritance.
    
- **Scalability** – Easy to add new features or classes.
    
- **Maintainability** – Easier to fix and update code.
    
- **Modularity** – Code is divided into smaller, independent parts (classes).
    
- **Real-world modeling** – Programs reflect real-life entities and relationships.
    

---

### **Summary**

|Concept|Description|Example|
|---|---|---|
|**Class**|Blueprint for creating objects|`class Car:`|
|**Object**|Instance of a class|`my_car = Car()`|
|**Encapsulation**|Hiding data within an object|Private variables|
|**Abstraction**|Showing essential details only|Abstract classes|
|**Inheritance**|Reusing properties/methods|`class Car(Vehicle):`|
|**Polymorphism**|Same method, different behavior|`animal.speak()`|