# 👻 Abstraction

> **Definition**: Abstraction is the process of hiding the complex implementation details of a system and exposing only the essential features to the user. It helps in reducing programming complexity and effort.

---

## 🛡️ Why do we need Abstraction?

1. **Simplicity**: Users interact with a simple interface without needing to understand the complex logic behind it.
2. **Security**: Hides background details and prevents unauthorized or accidental changes to the core system.
3. **Maintainability**: You can change the internal implementation without affecting the users of the abstraction.
4. **Focus**: Allows the developer to focus on *what* the object does instead of *how* it does it.

---

## 💻 Real-World Example

Think of driving a **Car**. 
- You know how to use the steering wheel, accelerator, and brakes (the **Interface**).
- You **do not need to know** how the engine combusts fuel, how the transmission shifts gears, or how the exhaust system works (the **Hidden Implementation Details**).

### ☕ Code Implementation (Java)

In object-oriented programming, Abstraction is achieved using **Abstract Classes** and **Interfaces**.

```java
// Abstract Class (The Concept)
abstract class Vehicle {
    // Abstract method (does not have a body)
    public abstract void startEngine();
    
    // Regular method
    public void stopEngine() {
        System.out.println("Engine stopped.");
    }
}

// Subclass (The Concrete Implementation)
class Car extends Vehicle {
    @Override
    public void startEngine() {
        // The complex implementation is hidden here!
        System.out.println("Car engine starting: Injecting fuel... Igniting spark plugs... VROOM!");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle myCar = new Car();
        
        // The user only calls startEngine(), without worrying about the internal mechanics!
        myCar.startEngine();
        myCar.stopEngine();
    }
}
```

---

## 🆚 Abstraction vs Encapsulation

These two are often confused in interviews! Here is the main difference:

| Feature | Abstraction | Encapsulation |
| :--- | :--- | :--- |
| **Focus** | Focuses on **what** the object should do. | Focuses on **how** the object does it. |
| **Concept** | Hiding the complex implementation details. | Wrapping data and methods into a single unit (hiding data). |
| **How to achieve** | Using Abstract classes and Interfaces. | Using Access Modifiers (`private`, `public`, `protected`). |
| **Analogy** | Knowing how to use the TV remote. | The plastic case that protects the TV's internal wires. |
