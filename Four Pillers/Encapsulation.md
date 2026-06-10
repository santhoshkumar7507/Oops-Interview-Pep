# 💊 Encapsulation

> **Interview Question**: What is Encapsulation?
> 
> **Answer**: Encapsulation is the process of binding data (variables) and methods (functions) together into a single unit (like a class) while restricting direct access to sensitive data. It improves security, maintainability, and data integrity.

---

## 📈 Advantages of Encapsulation

1. **Data Security**: Protects internal state.
2. **Better Control**: Allows you to validate data before changing it.
3. **Easy Maintenance**: Changes in one part of the code don't break other parts.
4. **Improved Flexibility**: You can make data read-only or write-only.

---

## 💻 Real-World Example
Think of an **ATM Machine**. 
You can interact with it to withdraw and deposit money, but you **cannot** directly modify the bank's internal database balance.

---

## 🐍 Python Example

In Python, we use double underscores `__` to make a variable private and prevent direct access from outside the class.

```python
class BankAccount:

    def __init__(self, owner, balance):
        self.owner = owner
        # The __ makes balance private
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount
        print(f"Deposited ₹{amount}")

    def withdraw(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
            print(f"Withdrawn ₹{amount}")
        else:
            print("Insufficient Balance")

    # Getter method to safely read the private data
    def get_balance(self):
        return self.__balance


# Usage
if __name__ == "__main__":
    account = BankAccount("John", 50000)

    account.deposit(10000)
    account.withdraw(5000)

    print("Current Balance: ₹", account.get_balance())
    
    # Trying to access account.__balance directly here would throw an error!
```
