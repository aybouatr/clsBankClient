# clsBankClient

## Overview

**clsBankClient** is a mini project written in C++ designed to practice and demonstrate the foundational concepts of Object-Oriented Programming (OOP) in a banking context. The project simulates a simple bank client management system, allowing users to manage bank accounts and perform basic operations such as creating clients, depositing, withdrawing, and viewing account information.

## Project Objectives

- Practice and strengthen understanding of key OOP principles in C++.
- Build a simple, clear, and extensible banking client system.
- Learn and apply encapsulation, inheritance, polymorphism, and abstraction in real-world scenarios.

## Object-Oriented Programming Concepts Used

This project leverages the following OOP concepts:

### 1. Classes and Objects
- **Classes** represent blueprints for real-world entities (e.g., BankClient, Account).
- **Objects** are instances of these classes, each representing a unique bank client or account.

### 2. Encapsulation
- Data members (such as account balance, client name) are declared as private or protected.
- Public methods (getters/setters) provide controlled access to internal data, ensuring data integrity.

### 3. Inheritance
- Common functionalities are grouped in base classes (e.g., Person or Account).
- Specialized classes (e.g., Client, SavingsAccount) inherit from base classes, reusing and extending behavior.

### 4. Polymorphism
- Functions can be overridden in derived classes to provide specific behavior (e.g., different account types may implement interest calculation differently).
- Enables flexible and scalable code, where new account types can be added easily.

### 5. Abstraction
- The system hides complex implementation details and exposes only essential features via public interfaces.
- Users interact with high-level methods, such as Deposit or Withdraw, without worrying about the internal logic.

## Why Use OOP?

- **Modularity:** Code is organized into separate, logical units (classes), making it easier to understand and maintain.
- **Reusability:** Common code is grouped in base classes and reused via inheritance, reducing duplication.
- **Extensibility:** New features (like new account types) can be added with minimal changes to existing code.
- **Maintainability:** Encapsulation protects data and logic, making bugs easier to locate and fix.

## How the Project Works

1. **Class Structure**
    - `BankClient` class encapsulates personal details and account information.
    - (Optionally) Base classes like `Person` or `Account` may be used for further abstraction.
    - Methods for depositing, withdrawing, and displaying information are implemented.

2. **Program Flow**
    - The user interacts with a menu-driven interface to choose actions (create client, deposit, withdraw, view info, etc.).
    - The program processes the input, updates objects accordingly, and outputs results.

3. **Example Usage**
    - Start the program.
    - Choose to create a new client by entering personal and account details.
    - Perform operations such as deposit or withdrawal.
    - View updated account information.
    - Exit the program.

## Example Code Snippet

```cpp
class BankClient {
private:
    std::string name;
    double balance;
public:
    BankClient(const std::string& clientName, double initialBalance)
        : name(clientName), balance(initialBalance) {}

    void Deposit(double amount) {
        balance += amount;
    }

    bool Withdraw(double amount) {
        if (amount > balance) return false;
        balance -= amount;
        return true;
    }

    void DisplayInfo() const {
        std::cout << "Client: " << name << ", Balance: $" << balance << std::endl;
    }
};
```

## How to Compile and Run

1. **Compile the Project:**
    ```sh
    g++ -std=c++11 -o clsBankClient main.cpp
    ```

2. **Run the Executable:**
    ```sh
    ./clsBankClient
    ```

## Project Structure

- `main.cpp` — Main program file with menu and user interaction logic.
- `BankClient.h`/`BankClient.cpp` — Class definition and implementation for bank clients.
- Additional headers and source files as needed for modularity and expansion.

## Conclusion

This project demonstrates how core OOP principles can be applied to build a simple, maintainable, and extensible banking client management system in C++. It serves as a practical exercise for anyone learning C++ or object-oriented design.

---
**Author:** aybouatr  
**License:** MIT (or specify your preferred license)
