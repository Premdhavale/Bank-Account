# 💰 BankAccount - Python OOP Example

This is a simple Python project demonstrating the concept of **Object-Oriented Programming (OOP)**, specifically **encapsulation**, using a `BankAccount` class.

## 🚀 Features

- Private account balance (`__balance`)
- Getter method to check balance
- Deposit and withdraw methods with validation
- Encapsulation with private variables
- Clean and readable code for beginners

## 🧾 Code Overview

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.__balance = balance  # Private attribute

    def get_balance(self):
        return self.__balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            return f"Deposited {amount}. New balance: {self.__balance}"
        else:
            return "Invalid deposit amount."

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            return f"Withdrew {amount}. New balance: {self.__balance}"
        else:
            return "Insufficient funds or invalid amount."
