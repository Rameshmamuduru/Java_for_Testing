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

# Java OOP Basics — Variables, Methods & Constructors

## 1. Variables in Java

A **variable** is a named memory location used to store a value.

### Basic syntax

```java
dataType variableName = value;
```

Example:

```java
int age = 25;
String username = "Ramesh";
boolean loginStatus = true;
```

---

# 2. Types of Variables

Java mainly has **3 types of variables** based on where they are declared.

1. Local Variable
2. Instance Variable
3. Static Variable

---

## 2.1 Local Variable

A variable declared **inside a method, constructor, or block** is called a local variable.

```java
class Login {

    void loginUser() {

        String username = "Ramesh";
        String password = "Password@123";

        System.out.println(username);
    }
}
```

Here:

```java
String username = "Ramesh";
String password = "Password@123";
```

are local variables.

### Important points

* Belongs to the method/block where it is declared.
* Can be directly accessed only within that scope.
* It does not belong to the object.
* It does not have a default value.
* It must be initialized before use.

Example:

```java
void testLogin() {

    String username;
    System.out.println(username);   // Compilation error
}
```

Correct:

```java
void testLogin() {

    String username = "Ramesh";
    System.out.println(username);
}
```

### Automation example

```java
void loginTest() {

    String username = "Ramesh";
    String password = "Password@123";

    System.out.println(username);
    System.out.println(password);
}
```

These values are required only for this particular method execution, so local variables are appropriate.

---

# 2.2 Instance Variable

A variable declared **inside a class but outside methods, constructors, and blocks**, without `static`, is an instance variable.

```java
class Login {

    String username;
    String password;
}
```

Here:

```java
String username;
String password;
```

are instance variables.

They belong to an **object**.

### Creating an object

```java
Login login = new Login();
```

Accessing instance variables:

```java
login.username = "Ramesh";
login.password = "Password@123";
```

Complete example:

```java
class Login {

    String username;
    String password;
}

class Main {

    public static void main(String[] args) {

        Login login = new Login();

        login.username = "Ramesh";
        login.password = "Password@123";

        System.out.println(login.username);
        System.out.println(login.password);
    }
}
```

### Important points

* Belongs to an object.
* Every object gets its **own copy**.
* Created when an object is created.
* Can have default values.
* Can be accessed using an object reference.

Example:

```java
Login user1 = new Login();
Login user2 = new Login();

user1.username = "Ramesh";
user2.username = "Suresh";
```

Now:

```text
user1.username → Ramesh
user2.username → Suresh
```

Each object has its own `username`.

---

# 2.3 Static Variable

A variable declared inside a class using `static` is called a static variable.

```java
class Login {

    static String application = "Banking Application";
}
```

A static variable belongs to the **class**, not to individual objects.

### Accessing static variable

Preferred way:

```java
Login.application
```

Example:

```java
class Login {

    static String application = "Banking Application";
}

class Main {

    public static void main(String[] args) {

        System.out.println(Login.application);
    }
}
```

### Important points

* Belongs to the class.
* Only one shared copy exists for the class.
* Shared by all objects.
* Preferred access is `ClassName.variableName`.
* Created when the class is loaded.

---

# 3. Instance vs Static Variables

| Feature    | Instance Variable | Static Variable      |
| ---------- | ----------------- | -------------------- |
| Belongs to | Object            | Class                |
| Copies     | One per object    | One shared copy      |
| Keyword    | No `static`       | `static`             |
| Access     | `object.variable` | `ClassName.variable` |
| Example    | username          | applicationName      |
| Data       | Object-specific   | Common/shared        |

### Example

```java
class Login {

    String username;                  // Instance
    static String application = "Bank"; // Static
}
```

```java
Login user1 = new Login();
Login user2 = new Login();

user1.username = "Ramesh";
user2.username = "Suresh";
```

```text
user1.username → Ramesh
user2.username → Suresh

Login.application → Bank
```

---

# 4. Methods in Java

A **method is a block of code defined inside a class that performs a specific operation/task.**

Basic syntax:

```java
returnType methodName(parameters) {

    // method body
}
```

Example:

```java
void login() {

    System.out.println("User logged in");
}
```

Here:

* `void` → return type
* `login` → method name
* `()` → parameter list
* `{ }` → method body

---

# 5. Why Methods Are Used

Methods help us:

* Reuse code
* Divide a program into smaller tasks
* Avoid duplicate code
* Improve readability
* Organize automation code

Example:

```java
void login() {
    System.out.println("Login");
}

void searchProduct() {
    System.out.println("Search Product");
}

void logout() {
    System.out.println("Logout");
}
```

Each method performs a specific task.

---

# 6. Four Basic Types of Methods

Methods can be understood using two questions:

1. Does the method accept parameters?
2. Does the method return a value?

This gives four types.

---

## Type 1: No Parameters + No Return Value

```java
void printMessage() {

    System.out.println("Hello");
}
```

Calling:

```java
printMessage();
```

The method:

* accepts nothing
* returns nothing

---

## Type 2: Parameters + No Return Value

```java
void printName(String name) {

    System.out.println(name);
}
```

Calling:

```java
printName("Ramesh");
```

Here:

```java
String name
```

is the parameter.

The method receives data but does not return a value.

---

## Type 3: No Parameters + Return Value

```java
int getNumber() {

    return 100;
}
```

Calling:

```java
int number = getNumber();
```

The method accepts nothing but returns an `int`.

---

## Type 4: Parameters + Return Value

```java
int add(int a, int b) {

    return a + b;
}
```

Calling:

```java
int result = add(10, 20);
```

Output:

```text
30
```

This is one of the most commonly used method types because it accepts input and produces output.

---

# 7. Method Parameters vs Arguments

### Parameter

The variable declared in the method definition:

```java
void login(String username) {
}
```

`username` is a **parameter**.

### Argument

The actual value passed during method calling:

```java
login("Ramesh");
```

`"Ramesh"` is an **argument**.

```text
Method definition → Parameter
Method call       → Argument
```

---

# 8. Method Return

If a method has a return type other than `void`, it must return a compatible value.

```java
int getAge() {

    return 25;
}
```

The return type is:

```java
int
```

and returned value is:

```java
25
```

Example:

```java
String getUsername() {

    return "Ramesh";
}
```

Calling:

```java
String username = getUsername();
```

---

# 9. Static Methods

A method declared using `static` belongs to the class.

```java
class Login {

    static void login() {

        System.out.println("Login");
    }
}
```

Call it using the class name:

```java
Login.login();
```

Static methods are commonly used for operations that do not require object-specific data.

---

# 10. Instance Methods

A method without `static` is an instance method.

```java
class Login {

    void login() {

        System.out.println("Login");
    }
}
```

To call it from another class:

```java
Login login = new Login();

login.login();
```

An object is required to call an instance method from outside the class.

---

# 11. Constructor

A **constructor is a special member of a class that is automatically executed when an object is created.**

Main purpose:

> Initialize an object's instance variables when the object is created.

Example:

```java
class Login {

    String username;
    String password;

    Login(String username, String password) {

        this.username = username;
        this.password = password;
    }
}
```

Creating the object:

```java
Login login = new Login("Ramesh", "Password@123");
```

The constructor executes automatically.

---

# 12. Constructor Rules

### Rule 1: Constructor name must match class name

```java
class Login {

    Login() {

    }
}
```

Correct.

---

### Rule 2: Constructor does not have a return type

Correct:

```java
Login() {

}
```

Incorrect as a constructor:

```java
void Login() {

}
```

The second one is a **method**, not a constructor.

---

### Rule 3: Constructor executes automatically during object creation

```java
Login login = new Login();
```

When:

```java
new Login()
```

executes, the constructor runs automatically.

---

# 13. No-Argument Constructor

A constructor that accepts no parameters is called a no-argument constructor.

```java
class Login {

    Login() {

        System.out.println("Login object created");
    }
}
```

Calling:

```java
Login login = new Login();
```

Output:

```text
Login object created
```

---

# 14. Parameterized Constructor

A constructor that accepts parameters is called a parameterized constructor.

```java
class Login {

    String username;
    String password;

    Login(String username, String password) {

        this.username = username;
        this.password = password;
    }
}
```

Creating an object:

```java
Login login = new Login("Ramesh", "Password@123");
```

The values are initialized during object creation.

---

# 15. Why Constructors Are Useful

Without a constructor:

```java
Login login = new Login();

login.username = "Ramesh";
login.password = "Password@123";
```

With a constructor:

```java
Login login = new Login("Ramesh", "Password@123");
```

Advantages:

* Initializes object data immediately
* Reduces separate assignment statements
* Makes object creation cleaner
* Makes required data clear
* Useful when creating multiple objects with different data

Example:

```java
Login user1 = new Login("Ramesh", "Password@123");
Login user2 = new Login("Suresh", "Password@456");
```

---

# 16. `this` Keyword

`this` refers to the **current object**.

It is commonly used when instance variables and parameters have the same name.

```java
class Login {

    String username;
    String password;

    Login(String username, String password) {

        this.username = username;
        this.password = password;
    }
}
```

Here:

```java
this.username
```

means the instance variable.

```java
username
```

means the constructor parameter.

Conceptually:

```text
this.username = username;
     ↑              ↑
instance variable  parameter
```

---

# 17. Constructor Overloading

A class can have multiple constructors as long as their parameter lists are different.

```java
class Login {

    Login() {

        System.out.println("No credentials");
    }

    Login(String username) {

        System.out.println(username);
    }

    Login(String username, String password) {

        System.out.println(username);
        System.out.println(password);
    }
}
```

These are different constructors because their parameter lists are different.

```java
new Login();

new Login("Ramesh");

new Login("Ramesh", "Password@123");
```

---

# 18. Default Constructor

If you do **not define any constructor**, Java provides a default no-argument constructor automatically.

Example:

```java
class Login {

    String username;
}
```

Java provides a default constructor behind the scenes.

Therefore:

```java
Login login = new Login();
```

works.

### Important

Once you create your own constructor:

```java
class Login {

    Login(String username) {

        this.username = username;
    }
}
```

Java will **not automatically provide** the no-argument constructor.

Therefore:

```java
Login login = new Login();
```

will give a compilation error.

You would need:

```java
Login login = new Login("Ramesh");
```

or explicitly create a no-argument constructor:

```java
Login() {

}
```

---

# 19. Constructor vs Method

| Feature               | Constructor                          | Method                    |
| --------------------- | ------------------------------------ | ------------------------- |
| Purpose               | Initialize object                    | Perform operation         |
| Name                  | Same as class                        | Any valid name            |
| Return type           | No return type                       | Has return type or `void` |
| Execution             | Automatically during object creation | Called explicitly         |
| Can accept parameters | Yes                                  | Yes                       |
| Can be overloaded     | Yes                                  | Yes                       |
| Main purpose          | Initialization                       | Behavior/operation        |

Example:

```java
class Login {

    String username;

    // Constructor
    Login(String username) {
        this.username = username;
    }

    // Method
    void displayUsername() {
        System.out.println(username);
    }
}
```

Usage:

```java
Login login = new Login("Ramesh");

login.displayUsername();
```

Flow:

```text
new Login("Ramesh")
        ↓
Constructor executes
        ↓
username initialized
        ↓
Object created
        ↓
login.displayUsername()
        ↓
Method executes
```

---

# 20. Variables + Constructor + Methods Together

This is an important combination to understand.

```java
class Login {

    // Instance variables
    String username;
    String password;

    // Constructor
    Login(String username, String password) {

        this.username = username;
        this.password = password;
    }

    // Method
    void login() {

        if (username.equals("Ramesh") &&
            password.equals("Password@123")) {

            System.out.println("Login Successful");

        } else {

            System.out.println("Invalid Credentials");
        }
    }
}
```

Main class:

```java
class Main {

    public static void main(String[] args) {

        Login user = new Login(
            "Ramesh",
            "Password@123"
        );

        user.login();
    }
}
```

### Execution flow

```text
new Login("Ramesh", "Password@123")
                ↓
        Constructor executes
                ↓
   username = Ramesh
   password = Password@123
                ↓
          Object created
                ↓
          user.login()
                ↓
        Login method executes
                ↓
        Login Successful
```

---

# 21. Automation Testing Connection

These concepts are heavily used when building automation frameworks.

Example:

```java
class LoginPage {

    String username;
    String password;

    LoginPage(String username, String password) {

        this.username = username;
        this.password = password;
    }

    void login() {

        System.out.println(
            "Login with: " + username
        );
    }
}
```

Creating different test data:

```java
LoginPage user1 =
    new LoginPage("Ramesh", "Password@123");

LoginPage user2 =
    new LoginPage("Suresh", "Password@456");
```

Each object contains its own instance data.

```text
user1
 ├── username → Ramesh
 └── password → Password@123

user2
 ├── username → Suresh
 └── password → Password@456
```

This is the foundation for understanding classes and objects used in automation frameworks such as Page Object Model.

---

# 22. Quick Revision

## Variables

```text
Local
  ↓
Inside method/block
  ↓
Limited scope

Instance
  ↓
Inside class, outside methods
  ↓
Belongs to object
  ↓
Each object has separate copy

Static
  ↓
Inside class with static
  ↓
Belongs to class
  ↓
One shared copy
```

## Methods

```text
Method
  ↓
Performs an operation
  ↓
Can accept parameters
  ↓
Can return a value
```

Four basic types:

```text
1. No parameter + No return
2. Parameter + No return
3. No parameter + Return
4. Parameter + Return
```

## Constructors

```text
Constructor
     ↓
Runs during object creation
     ↓
Initializes object
     ↓
Same name as class
     ↓
No return type
     ↓
Can have parameters
     ↓
Can be overloaded
```

---

# 23. Most Important Interview Points

Remember these clearly:

1. Java has **local, instance, and static variables**.
2. Local variables belong to their method/block.
3. Instance variables belong to an object.
4. Static variables belong to the class.
5. Each object has its own instance-variable values.
6. Static variables are shared.
7. A method performs a specific operation.
8. Methods can accept parameters and return values.
9. A constructor initializes an object.
10. A constructor has the same name as the class.
11. A constructor has no return type.
12. A constructor executes automatically when an object is created.
13. Constructors can be overloaded.
14. `this` refers to the current object.
15. `this.variable = parameter` is commonly used when both have the same name.
16. If no constructor is written, Java provides a default no-argument constructor.
17. Once a constructor is explicitly written, Java does not automatically provide the no-argument constructor.
18. Constructor = **object initialization**.
19. Method = **operation/behavior**.
20. Instance variable = **object-specific data**.
21. Static variable = **shared class-level data**.
