# 🎭 Polymorphism

> **Interview Question**: What is Polymorphism?
> 
> **Answer**: Polymorphism means "Many Forms". It allows the same interface or method to behave differently depending on the object calling it. It provides flexibility and enables runtime decision-making.

---

## 📈 Advantages of Polymorphism

1. **Flexibility**
2. **Scalability**
3. **Better Code Design**
4. **Easy Extension**

---

## 💻 Real-World Example
**A Start Button**
- Car -> Starts Engine
- Computer -> Starts Operating System
- Washing Machine -> Starts Washing Cycle

---

## 🐍 Python Example

```python
class Dog:
    def sound(self):
        print("Bark Bark")

class Cat:
    def sound(self):
        print("Meow Meow")

# Usage
animals = [Dog(), Cat()]

for animal in animals:
    animal.sound()
```
