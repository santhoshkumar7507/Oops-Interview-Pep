Interview Question

Q: What is Inheritance?

<!-- Answer -->

Inheritance allows one class to acquire properties and methods of another class. It promotes code reusability and reduces duplication.

<!-- Problems  -->

class Animal:

    def eat(self):
        print("Eating")


class Dog(Animal):

    def bark(self):
        print("Barking")


d = Dog()

d.eat()
d.bark()