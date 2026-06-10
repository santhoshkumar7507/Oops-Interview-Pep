# 🧬 Inheritance

> **Interview Question**: What is Inheritance?
> 
> **Answer**: Inheritance is an OOP concept where a child class inherits attributes and methods from a parent class. It promotes code reusability and establishes an 'is-a' relationship.

---

## 📈 Advantages of Inheritance

1. **Code Reusability**
2. **Reduced Redundancy**
3. **Easy Maintenance**
4. **Better Extensibility**

---

## 💻 Real-World Example
**Animal -> Dog**
A Dog inherits common characteristics from the Animal class.

---

## 🐍 Python Example

```python
class Animal:
    def eat(self):
        print("Animal is Eating")

class Dog(Animal):
    def bark(self):
        print("Dog is Barking")

# Usage
dog = Dog()

dog.eat()
dog.bark()
```
