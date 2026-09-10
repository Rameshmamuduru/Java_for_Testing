## OOPS:

OOPs (Object-Oriented Programming System), usually called OOP (Object-Oriented Programming), is a way of writing Java programs by organizing code around objects and classes.

**Pillers of OOPS**

| OOP Concept       | Simple meaning                                                           |
| ----------------- | ------------------------------------------------------------------------ |
| **Class**         | A blueprint/template used to create objects                              |
| **Object**        | An actual instance of a class that contains data and can perform actions |
| **Encapsulation** | Binding data and methods together and controlling access                 |
| **Inheritance**   | One class acquiring properties/methods from another class                |
| **Polymorphism**  | One thing behaving in different ways                                     |
| **Abstraction**   | Hiding implementation details and showing only what is necessary         |

### Class, Object and Methods:

**1. Class**

A class is a **user-defined reference data** type that acts as a **blueprint for creating objects**. It contains variables (data/state) and methods (behavior) that define the characteristics and functionality of its objects.

**2. Object**

An object is an instance of a class that has its own state and can access the behavior defined by that class.

**3. Methods**

A method is a named block of code defined inside a class that performs a specific operation or behavior. It can accept input through parameters and may return a value.

**Mind Map**

```
                 CLASS
                  │
        ┌─────────┴─────────┐
        │                   │
     VARIABLES            METHODS
     (State)             (Behavior)
        │                   │
        └─────────┬─────────┘
                  │
             creates
                  ↓
                OBJECT
                  │
        ┌─────────┴─────────┐
        ↓                   ↓
   has its own data    performs actions
```

### Example:

**1. Creating a Main class**
```JAVA
class BankAccount {

    String accountHolder;
    double balance;

    void deposit(double amount) {
        balance = balance + amount;
    }

    void displayBalance() {
        System.out.println("Balance: " + balance);
    }
}
```

- It defines:
  - **Variables** → accountHolder, balance
  - **Methods** → deposit(), displayBalance()

**2. Another class uses Bank Account:**

``` JAVA
class Main {

    public static void main(String[] args) {

        BankAccount account1 = new BankAccount();

        account1.accountHolder = "Ramesh";
        account1.balance = 10000;

        account1.deposit(5000);

        account1.displayBalance();
    }
}
```
**MIND MAP**

```
BankAccount class
       │
       │ Defines
       ↓
  What an account
  has and can do
       
       ↓

Main class
       │
       │ Creates/uses
       ↓
  BankAccount object
```
**Creation of Methods in the Class**
``` JAVA
public class StringMethods {

    static void printMessage() {
        System.out.println("Hello Ramesh");
    }

    public static void main(String[] args) {

        printMessage();
    }
}
```

























