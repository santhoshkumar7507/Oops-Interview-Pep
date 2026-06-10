# 👻 Abstraction

> **Interview Question**: What is Abstraction?
> 
> **Answer**: Abstraction means hiding implementation details and showing only essential features to the user. It focuses on *what* an object does rather than *how* it does it.

---

## 📈 Advantages of Abstraction

1. **Reduces Complexity**
2. **Improves Readability**
3. **Better Security**
4. **Easier Maintenance**

---

## 💻 Real-World Example
**Driving a Car**
A driver uses the steering wheel, brakes, and accelerator without needing to know the internal engine mechanism.

---

## 🐍 Python Example

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

class Car(Vehicle):
    def start(self):
        print("Car Started Successfully")

# Usage
car = Car()
car.start()
```
