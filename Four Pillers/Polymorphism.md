# 🎭 Polymorphism

> **Interview Question**: What is Polymorphism?
> 
> **Answer**: Polymorphism comes from two Greek words: *poly* (many) and *morphs* (forms). It means "one interface, multiple forms." In programming, it allows the same method to behave differently depending on the object that is calling it.

---

## 🐍 Python Example

In Python, polymorphism is highly flexible. You can define the same method in different classes, and Python will know which one to call based on the object type!

```python
# 1. First Class
class Dog:
    def sound(self):
        return "🐕 Woof woof!"

# 2. Second Class with the SAME method name
class Cat:
    def sound(self):
        return "🐈 Meow meow!"

# 3. A common interface/function that uses Polymorphism
def make_animal_sound(animal):
    # Notice how we call .sound() without knowing if it's a Dog or a Cat!
    print(animal.sound())

# Usage
if __name__ == "__main__":
    dog = Dog()
    cat = Cat()

    # The same function behaves differently depending on the object!
    make_animal_sound(dog)  # Output: 🐕 Woof woof!
    make_animal_sound(cat)  # Output: 🐈 Meow meow!
```

---

## 🔄 Types of Polymorphism (Important for Interviews)

In traditional OOP languages like Java or C++, polymorphism is strictly divided into two types:

### 1. Compile-Time Polymorphism (Static Binding)
Achieved through **Method Overloading**.
*Example: Having two methods named `add()`, but one takes 2 numbers and the other takes 3 numbers.*
*(Note: Python does not natively support true Method Overloading, but we can mimic it using default arguments).*

### 2. Run-Time Polymorphism (Dynamic Binding)
Achieved through **Method Overriding**.
*Example: A child class providing a specific implementation of a method that is already provided by its parent class.*
