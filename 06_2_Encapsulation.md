# Java OOP — Encapsulation

## 1. What is Encapsulation?

**Encapsulation** is the OOP concept of **binding data (variables) and the methods that operate on that data into a single class, while controlling direct access to the data.**

In simple terms:

> **Keep data protected and provide controlled access through methods.**

Example:

```java
class Login {

    private String username;
    private String password;

    void setUsername(String username) {
        this.username = username;
    }

    String getUsername() {
        return username;
    }
}
```

Here:

```text
username
password
   ↓
private data
   ↓
Access through methods
   ↓
setUsername()
getUsername()
```

---

# 2. Why Do We Need Encapsulation?

Without encapsulation:

```java
class Login {

    String password;
}
```

Anyone with access to the object can directly change it:

```java
Login login = new Login();

login.password = "WrongPassword";
```

There is no control over how the value is changed.

With encapsulation:

```java
class Login {

    private String password;

    void setPassword(String password) {

        if (password.length() >= 8) {
            this.password = password;
        }
    }

    String getPassword() {
        return password;
    }
}
```

Now the class controls how the password is assigned.

---

# 3. Main Components of Encapsulation

Encapsulation commonly involves:

```text
Encapsulation
     │
     ├── Data hiding
     │      ↓
     │   private variables
     │
     └── Controlled access
            ↓
       public/protected methods
       such as getters/setters
```

The most common implementation is:

```java
private variables
+
public getters/setters
```

---

# 4. `private` Keyword

`private` restricts direct access to a variable or method from outside its class.

Example:

```java
class User {

    private String username;
}
```

This will not work from another class:

```java
User user = new User();

user.username = "Ramesh";
```

Because `username` is private.

The compiler gives an access error.

---

# 5. Getter Method

A **getter** is a method used to retrieve/read the value of a private variable.

Example:

```java
class User {

    private String username;

    public String getUsername() {

        return username;
    }
}
```

Calling:

```java
User user = new User();

System.out.println(user.getUsername());
```

Flow:

```text
private username
       ↓
 getUsername()
       ↓
    returns
       ↓
   caller
```

---

# 6. Setter Method

A **setter** is a method used to assign/change the value of a private variable.

Example:

```java
class User {

    private String username;

    public void setUsername(String username) {

        this.username = username;
    }
}
```

Calling:

```java
User user = new User();

user.setUsername("Ramesh");
```

Flow:

```text
"Ramesh"
    ↓
setUsername()
    ↓
private username
```

---

# 7. Getter + Setter Together

Complete example:

```java
class User {

    private String username;
    private String password;

    public void setUsername(String username) {

        this.username = username;
    }

    public String getUsername() {

        return username;
    }

    public void setPassword(String password) {

        this.password = password;
    }

    public String getPassword() {

        return password;
    }
}
```

Using the class:

```java
class Main {

    public static void main(String[] args) {

        User user = new User();

        user.setUsername("Ramesh");
        user.setPassword("Password@123");

        System.out.println(user.getUsername());
        System.out.println(user.getPassword());
    }
}
```

---

# 8. Why Not Make Variables Public?

You could do:

```java
class User {

    public String age;
}
```

Then:

```java
user.age = "-100";
```

There is no validation.

With encapsulation:

```java
class User {

    private int age;

    public void setAge(int age) {

        if (age >= 0) {
            this.age = age;
        }
    }

    public int getAge() {

        return age;
    }
}
```

Now the class can control the data.

```java
user.setAge(-100);
```

The class can reject the invalid value.

This is one of the major benefits of encapsulation:

> **Controlled access and validation.**

---

# 9. Encapsulation Does NOT Mean Only Getters and Setters

A common misunderstanding is:

> Encapsulation = private variables + getters + setters.

That is the **common implementation**, but the concept is broader.

Encapsulation means:

> **The class controls how its internal data is accessed and modified.**

You don't necessarily need to provide both getter and setter.

### Read-only data

```java
class Account {

    private String accountNumber;

    public String getAccountNumber() {

        return accountNumber;
    }
}
```

There is no setter.

Therefore, outside code can read it but cannot directly modify it.

### Write-controlled data

You can also provide a setter without exposing the value through a getter.

---

# 10. Encapsulation vs Data Hiding

These concepts are related but not exactly identical.

### Data Hiding

Preventing direct access to internal data.

Usually achieved using:

```java
private
```

### Encapsulation

Bundling data and related behavior together and controlling access to them.

```text
Data Hiding
    ↓
private variables

Encapsulation
    ↓
Data + methods
    ↓
Controlled access
```

A useful interview explanation:

> **Data hiding focuses on restricting access, while encapsulation focuses on bundling data and behavior and providing controlled access.**

---

# 11. `this` Keyword in Encapsulation

Setters commonly use `this`.

```java
class User {

    private String username;

    public void setUsername(String username) {

        this.username = username;
    }
}
```

There are two `username`s:

```text
this.username
      ↓
instance variable

username
      ↓
method parameter
```

Therefore:

```java
this.username = username;
```

means:

> Assign the parameter value to the current object's instance variable.

---

# 12. Encapsulation with Constructor

Encapsulation can also be combined with constructors.

```java
class User {

    private String username;
    private String password;

    User(String username, String password) {

        this.username = username;
        this.password = password;
    }

    public String getUsername() {

        return username;
    }

    public void setPassword(String password) {

        this.password = password;
    }
}
```

Creating the object:

```java
User user =
    new User("Ramesh", "Password@123");
```

The constructor initializes the private data.

Then methods provide controlled access.

---

# 13. Encapsulation + Validation

This is one of the most useful practical applications.

```java
class Login {

    private String username;
    private String password;

    public void setUsername(String username) {

        if (username != null && !username.isBlank()) {
            this.username = username;
        }
    }

    public void setPassword(String password) {

        if (password != null && password.length() >= 8) {
            this.password = password;
        }
    }

    public String getUsername() {

        return username;
    }
}
```

Now invalid data can be rejected.

```text
Input
  ↓
Setter
  ↓
Validation
  ↓
Valid? ── Yes ──> Store data
  │
  No
  ↓
Reject
```

This is why encapsulation is useful for protecting the object's state.

---

# 14. Encapsulation in Automation Testing

Encapsulation is heavily used in automation frameworks.

Consider a login page.

```java
class LoginPage {

    private String username;
    private String password;

    public void enterUsername(String username) {

        this.username = username;
        System.out.println("Entered username");
    }

    public void enterPassword(String password) {

        this.password = password;
        System.out.println("Entered password");
    }

    public void clickLogin() {

        System.out.println("Clicked Login");
    }
}
```

Test class:

```java
class LoginTest {

    public static void main(String[] args) {

        LoginPage loginPage = new LoginPage();

        loginPage.enterUsername("Ramesh");
        loginPage.enterPassword("Password@123");
        loginPage.clickLogin();
    }
}
```

The test does not directly manipulate the internal data.

It uses the methods provided by the page class.

```text
LoginTest
    ↓
enterUsername()
enterPassword()
clickLogin()
    ↓
LoginPage
    ↓
Internal data / implementation
```

This makes automation code easier to maintain because the internal implementation can change without requiring every test to know the details.

---

# 15. Encapsulation in Page Object Model

This is especially important for **POM (Page Object Model)**.

For example:

```java
class LoginPage {

    private String usernameLocator;
    private String passwordLocator;
    private String loginButtonLocator;

    public void enterUsername(String username) {
        // locate username field
    }

    public void enterPassword(String password) {
        // locate password field
    }

    public void clickLogin() {
        // locate and click login button
    }
}
```

The test should use:

```java
loginPage.enterUsername("Ramesh");
loginPage.enterPassword("Password@123");
loginPage.clickLogin();
```

rather than knowing the internal locator implementation.

Therefore:

> **POM uses encapsulation to hide page implementation details and expose meaningful actions to test classes.**

---

# 16. Real-Time Example

Think about an ATM.

You don't directly access the bank's internal balance database.

You perform controlled operations:

```text
ATM
 │
 ├── checkBalance()
 ├── withdraw()
 ├── deposit()
 └── transfer()
```

Internally, the banking system manages:

```text
Account balance
Transaction status
Account rules
Security checks
```

Those internal details are protected.

You interact through controlled operations.

This is the basic idea behind encapsulation.

---

# 17. Encapsulation vs Abstraction

These two are commonly confused.

### Encapsulation

Focus:

> **How do we protect/control access to data and implementation?**

Example:

```java
private String password;
```

with controlled methods.

### Abstraction

Focus:

> **What should the user see/use, while hiding unnecessary implementation details?**

Example:

```java
login();
```

The caller doesn't need to know every internal step involved in logging in.

Simple distinction:

```text
Encapsulation
     ↓
Protect + control access

Abstraction
     ↓
Hide unnecessary implementation complexity
```

---

# 18. Access Modifiers Used with Encapsulation

Java provides four main access levels:

| Modifier    | Same Class | Same Package |         Child Class | Other Package |
| ----------- | ---------: | -----------: | ------------------: | ------------: |
| `private`   |        Yes |           No |                 No* |            No |
| default     |        Yes |          Yes | Yes if same package |            No |
| `protected` |        Yes |          Yes |                 Yes |       Limited |
| `public`    |        Yes |          Yes |                 Yes |           Yes |

For basic encapsulation, the most important combination to understand is:

```java
private
```

for internal data and controlled methods such as:

```java
public
```

getters/setters or business methods.

---

# 19. Benefits of Encapsulation

### 1. Data protection

Internal data cannot be directly modified.

### 2. Controlled access

The class decides how data is accessed.

### 3. Validation

Invalid data can be rejected.

### 4. Maintainability

Internal implementation can change without affecting callers.

### 5. Better organization

Data and related operations remain together inside the class.

### 6. Reduced coupling

Other classes depend on the exposed methods rather than internal implementation details.

---

# 20. Complete Example

```java
class BankAccount {

    private String accountNumber;
    private double balance;

    BankAccount(String accountNumber, double balance) {

        this.accountNumber = accountNumber;
        this.balance = balance;
    }

    public String getAccountNumber() {

        return accountNumber;
    }

    public double getBalance() {

        return balance;
    }

    public void deposit(double amount) {

        if (amount > 0) {
            balance = balance + amount;
        }
    }

    public void withdraw(double amount) {

        if (amount > 0 && amount <= balance) {
            balance = balance - amount;
        }
    }
}
```

Usage:

```java
class Main {

    public static void main(String[] args) {

        BankAccount account =
            new BankAccount("ACC123", 10000);

        account.deposit(2000);
        account.withdraw(3000);

        System.out.println(account.getBalance());
    }
}
```

Notice that this is **not allowed**:

```java
account.balance = -5000;
```

because `balance` is private.

Instead:

```java
account.deposit(2000);
account.withdraw(3000);
```

The class controls how the balance changes.

---

# 21. Encapsulation — Quick Revision

```text
                 ENCAPSULATION
                       │
          ┌────────────┴────────────┐
          │                         │
      Data hiding              Controlled access
          │                         │
       private                 methods
          │                         │
          └────────────┬────────────┘
                       ↓
              Protected object state
```

Typical implementation:

```java
class User {

    private String username;

    public void setUsername(String username) {
        this.username = username;
    }

    public String getUsername() {
        return username;
    }
}
```

---

# 22. Important Interview Questions

### Q1. What is encapsulation?

> Encapsulation is the OOP concept of bundling data and the methods that operate on that data into a class while controlling access to the internal data.

### Q2. How do you achieve encapsulation in Java?

> Commonly by declaring instance variables as `private` and providing controlled access through public methods such as getters, setters, or business methods.

### Q3. Why are variables made private?

> To prevent direct external access and allow the class to control how the data is accessed or modified.

### Q4. What is a getter?

> A method used to retrieve the value of a private variable.

### Q5. What is a setter?

> A method used to assign or modify the value of a private variable.

### Q6. Is encapsulation only about getters and setters?

> No. Getters and setters are a common implementation. The core idea is bundling data and behavior and controlling access to the object's internal state.

### Q7. What is the difference between encapsulation and data hiding?

> Data hiding restricts access to internal data, while encapsulation bundles data and behavior and provides controlled access.

### Q8. How is encapsulation useful in automation?

> It hides internal implementation details such as page elements and exposes meaningful actions such as `login()`, `enterUsername()`, and `clickLogin()`.

---

# 23. Practice Questions — Encapsulation

## Level 1 — Basic Understanding

### Q1

What is encapsulation?

Explain it in your own words.

### Q2

Why do we use the `private` keyword for instance variables?

### Q3

What is the difference between a getter and a setter?

### Q4

Is the following class properly encapsulated?

```java
class Student {

    public String name;
    public int age;
}
```

Explain why or why not.

---

# Level 2 — Getters and Setters

### Q5

Create a `Student` class with:

```text
private String name
private int age
```

Create:

```text
setName()
getName()
setAge()
getAge()
```

Create an object and assign/read the values.

### Q6

Create a `Login` class with:

```text
private String username
private String password
```

Create getters and setters.

### Q7

Modify the password setter so that a password must contain at least **8 characters**.

Reject shorter passwords.

---

# Level 3 — Encapsulation + Constructor

### Q8

Create a `BankAccount` class containing:

```text
private String accountNumber
private double balance
```

Initialize them using a constructor.

Create:

```text
getAccountNumber()
getBalance()
deposit()
withdraw()
```

Prevent withdrawal when the amount is greater than the balance.

---

# Level 4 — Automation Testing

### Q9

Create a `LoginPage` class with private fields:

```text
username
password
loginButton
```

Create public methods:

```text
enterUsername()
enterPassword()
clickLogin()
```

The test class should interact only through these methods.

---

### Q10

Create a `CheckoutPage` class with private data:

```text
productName
quantity
price
```

Create methods:

```text
addProduct()
increaseQuantity()
getTotalPrice()
```

The test class should not directly modify the private variables.

---

# Level 5 — Interview Challenge

### Q11

Explain the difference between:

```java
class User {

    public String username;
}
```

and:

```java
class User {

    private String username;

    public void setUsername(String username) {
        this.username = username;
    }

    public String getUsername() {
        return username;
    }
}
```

Why is the second approach better?

---

### Q12 — Final Challenge

Build a small **Bank Account automation simulation**.

Requirements:

```text
BankAccount
│
├── private accountNumber
├── private balance
│
├── constructor
├── getAccountNumber()
├── getBalance()
├── deposit()
└── withdraw()
```

Rules:

1. Account number should be initialized through the constructor.
2. Balance must be private.
3. Deposit amount must be greater than 0.
4. Withdrawal amount must be greater than 0.
5. Withdrawal must not exceed the balance.
6. Test everything from a separate `Main` class.
7. You should never directly access `balance`.

This exercise will test:

**private variables + constructors + getters + methods + validation + encapsulation.**
