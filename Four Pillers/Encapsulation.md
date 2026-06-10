# 💊 Encapsulation

> **Definition**: Encapsulation is the mechanism of hiding data implementation by restricting direct access to it. It binds together the data (variables) and the methods (functions) that manipulate the data into a single unit (like a class), keeping both safe from outside interference and misuse.

---

## 🛡️ Why do we need Encapsulation?

1. **Data Protection (Data Hiding)**: It protects the internal state of an object by hiding its attributes from the outside world.
2. **Security & Control**: You can make variables **read-only** or **write-only** by providing only `getter` or `setter` methods. You can also add validation logic inside setters!
3. **Flexibility**: The internal implementation of the class can be changed without affecting the other parts of the code that use it.
4. **Maintainability**: Encapsulated code is loosely coupled, making it highly reusable, easier to debug, and simpler to test.

---

## 💻 Real-World Example

Think of a **Bank Account**. You don't want anyone (or any other part of the program) to directly modify your account balance by just doing `account.balance = 1000000;`. 

The only way the balance should change is through secure, controlled `deposit()` and `withdraw()` methods!

### ☕ Code Implementation (Java)

```java
class BankAccount {
    // 1. Private data (Hidden from the outside world)
    private double balance;  

    // Constructor
    public BankAccount(double initialBalance) {
        if (initialBalance > 0) {
            this.balance = initialBalance;
        }
    }

    // 2. Public Methods (The "Interface" to interact with the data)
    
    // Deposit Method with Validation
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: $" + amount);
        } else {
            System.out.println("Invalid deposit amount.");
        }
    }

    // Withdraw Method with Validation
    public void withdraw(double amount) {
        if (amount > 0 && balance >= amount) {
            balance -= amount;
            System.out.println("Withdrew: $" + amount);
        } else {
            System.out.println("Insufficient funds or invalid amount!");
        }
    }

    // Getter for Balance (Read-only access)
    public double getBalance() {
        return balance;
    }
}
```

---

## 🔑 Access Modifiers in Encapsulation

Encapsulation relies heavily on **Access Modifiers** to control visibility. To achieve true encapsulation, class variables should ideally be `private`.

| Modifier | Inside Class | Same Package | Subclass | Outside Package |
| :--- | :---: | :---: | :---: | :---: |
| `private` | ✅ | ❌ | ❌ | ❌ |
| `default` | ✅ | ✅ | ❌ | ❌ |
| `protected`| ✅ | ✅ | ✅ | ❌ |
| `public` | ✅ | ✅ | ✅ | ✅ |
