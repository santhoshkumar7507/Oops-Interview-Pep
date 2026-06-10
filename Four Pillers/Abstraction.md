# 👻 Abstraction

> **Interview Question**: What is Abstraction?
> 
> **Answer**: Abstraction means hiding the internal implementation details and showing only the essential features to the user. It helps in reducing programming complexity and effort.

---

## 🐍 Python Example

In Python, we achieve abstraction using the `abc` (Abstract Base Classes) module.

```python
from abc import ABC, abstractmethod

# 1. Abstract Class
class Vehicle(ABC):
    
    # Abstract method: It has no body!
    # Any class that inherits Vehicle MUST implement this method.
    @abstractmethod
    def start(self):
        pass


# 2. Concrete Class
class Car(Vehicle):
    
    # Implementing the abstract method
    def start(self):
        print("🚗 Car Started: Vroom vroom!")


# Usage
if __name__ == "__main__":
    c = Car()
    c.start()
```

### 🧠 Why is this useful?
In the example above, the `Vehicle` class enforces a rule: *Every vehicle must have a `start` method*. But it leaves the actual implementation (the complex details) to the specific `Car` class. 

The user only cares that they can call `c.start()`, without worrying about how the `Car` actually starts internally!
