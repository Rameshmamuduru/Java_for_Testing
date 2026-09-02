# JAVA
## 1. What is Java?

**Java is a high-level, object-oriented, platform-independent programming language used to develop applications.**

Java is widely used for:

* Web applications
* Enterprise applications
* Android applications
* Backend systems
* Automation testing

---

# 2. Features of Java

| Feature                  | Simple Meaning                                                                        |
| ------------------------ | ------------------------------------------------------------------------------------- |
| **Simple**               | Easy to learn compared with many low-level languages                                  |
| **Object-Oriented**      | Programs are designed using classes and objects                                       |
| **Platform Independent** | Java code can run on different operating systems using the JVM                        |
| **Portable**             | Java programs can be moved between systems with minimal changes                       |
| **Secure**               | Provides security features such as bytecode verification and controlled memory access |
| **Robust**               | Strong memory management and exception handling make programs more reliable           |
| **Multithreaded**        | Can execute multiple tasks at the same time                                           |
| **High Performance**     | JVM uses techniques such as JIT compilation to improve execution speed                |
| **Distributed**          | Supports development of network/distributed applications                              |
| **Architecture Neutral** | Java bytecode is not tied to a specific processor architecture                        |
| **Dynamic**              | Classes and resources can be loaded at runtime                                        |

### Important interview point

The famous Java concept is:

```text
Write Once, Run Anywhere
```

Java source code is compiled into **bytecode**, and the **JVM** executes that bytecode on different operating systems.

---

# 3. What is a Data Type?

A **data type** specifies **what kind of value a variable can store**.

Example:

```java
int age = 25;
```

Here:

* `int` → data type
* `age` → variable
* `25` → value

Java data types are broadly divided into:

```text
Data Types
│
├── Primitive Data Types
│
└── Non-Primitive / Reference Data Types
```

---

# 4. Primitive Data Types

Java has **8 primitive data types**.

| Data Type | What it stores                        |
| --------- | ------------------------------------- |
| `byte`    | Small whole numbers                   |
| `short`   | Whole numbers larger than `byte`      |
| `int`     | Integer/whole numbers                 |
| `long`    | Large whole numbers                   |
| `float`   | Decimal numbers with single precision |
| `double`  | Decimal numbers with double precision |
| `char`    | A single character                    |
| `boolean` | `true` or `false`                     |

### Remember

```text
8 Primitive Data Types

byte
short
int
long
float
double
char
boolean
```

---

# 5. Non-Primitive / Derived Data Types

Non-primitive types are also commonly called **reference types**.

Examples include:

* `String`
* Arrays
* Classes
* Objects
* Interfaces
* Enums

There isn't a fixed count like the **8 primitive types**, because reference types can be created/defined by programmers.

For now, since you're learning Java for testing, **focus on the 8 primitive types first.**

---

# 6. Simple Practice — Primitive Data Types

Try each of these individually.

### `byte`

```java
public class BytePractice {
    public static void main(String[] args) {

        byte age = 25;

        System.out.println(age);
    }
}
```

---

### `short`

```java
public class ShortPractice {
    public static void main(String[] args) {

        short salary = 30000;

        System.out.println(salary);
    }
}
```

---

### `int`

```java
public class IntPractice {
    public static void main(String[] args) {

        int population = 100000;

        System.out.println(population);
    }
}
```

---

### `long`

```java
public class LongPractice {
    public static void main(String[] args) {

        long distance = 123456789L;

        System.out.println(distance);
    }
}
```

Notice the **`L`**.

---

### `float`

```java
public class FloatPractice {
    public static void main(String[] args) {

        float temperature = 36.5f;

        System.out.println(temperature);
    }
}
```

Notice the **`f`**.

---

### `double`

```java
public class DoublePractice {
    public static void main(String[] args) {

        double price = 999.99;

        System.out.println(price);
    }
}
```

---

### `char`

```java
public class CharPractice {
    public static void main(String[] args) {

        char grade = 'A';

        System.out.println(grade);
    }
}
```

Remember:

```java
'A'
```

uses **single quotes**.

---

### `boolean`

```java
public class BooleanPractice {
    public static void main(String[] args) {

        boolean isLoggedIn = true;

        System.out.println(isLoggedIn);
    }
}
```

A boolean can contain:

```java
true
false
```

---

# 7. What is a Variable?

A **variable is a named memory location used to store a value**.

Example:

```java
int age = 25;
```

Here:

```text
int       → Data type
age       → Variable name
25        → Value
=         → Assignment operator
```

### General syntax

```java
dataType variableName = value;
```

Example:

```java
int age = 25;
double salary = 50000.50;
char grade = 'A';
boolean status = true;
```

---

# 8. What is Type Casting?

**Type casting is the process of explicitly converting a value from one data type to another data type.**

Example:

```java
double price = 99.99;

int value = (int) price;
```

Here:

```java
(int)
```

is the **cast**.

The result is:

```text
99.99 → 99
```

The decimal part is lost.

---

# 9. Types of Casting

There are two important types:

```text
Type Casting
│
├── Widening Casting
│
└── Narrowing Casting
```

---

## 9.1 Widening Casting

**Widening means converting a smaller type into a larger type.**

Example:

```java
int number = 100;

double value = number;

System.out.println(value);
```

Output:

```text
100.0
```

Here:

```text
int → double
```

Java automatically performs the conversion.

So widening is:

* Smaller → larger
* Automatic
* No explicit cast normally required

```java
int number = 100;
double value = number;
```

You don't need:

```java
double value = (double) number;
```

---

## 9.2 Narrowing Casting

**Narrowing means converting a larger type into a smaller type.**

Example:

```java
double number = 100.75;

int value = (int) number;

System.out.println(value);
```

Output:

```text
100
```

Here:

```text
double → int
```

The decimal `.75` is lost.

Therefore narrowing requires **explicit casting**:

```java
(int) number
```

---

# 10. Widening vs Narrowing

|                | Widening             | Narrowing               |
| -------------- | -------------------- | ----------------------- |
| Direction      | Smaller → Larger     | Larger → Smaller        |
| Example        | `int → double`       | `double → int`          |
| Automatic?     | Usually yes          | No                      |
| Explicit cast? | Usually not required | Required                |
| Data loss      | Generally avoided    | Possible                |
| Example        | `double d = number;` | `int x = (int) number;` |

### Easy memory trick

```text
WIDENING
Small → Big
⬆️

NARROWING
Big → Small
⬇️
```

---

# 11. Type Conversion vs Type Casting

This is where the terms can become confusing.

### Type Conversion

**Type conversion is the general process of changing one data type into another.**

### Type Casting

**Type casting is explicitly telling Java to treat/convert a value as another type using `(dataType)`.**

Example:

```java
double price = 99.99;

int amount = (int) price;
```

This involves:

```text
Type conversion → double to int
       +
Type casting → (int)
       +
Narrowing → larger to smaller
```

### Very simple rule

> **Conversion = changing the type**
> **Casting = explicitly telling Java to change the type**

---

# 12. Primitive Type Precedence / Promotion

For the primitive numeric types, a useful order to remember is:

| Order | Type     |
| ----: | -------- |
|     1 | `byte`   |
|     2 | `short`  |
|     3 | `int`    |
|     4 | `long`   |
|     5 | `float`  |
|     6 | `double` |

This represents the **general widening direction**:

```text
byte
  ↓
short
  ↓
int
  ↓
long
  ↓
float
  ↓
double
```

`char` is also an integral type and can participate in numeric promotion, while `boolean` is separate and **cannot be converted to/from numeric types**.

### Important

Don't interpret this table as saying every conversion is equally safe in terms of precision. For example, `long → float` is a widening conversion but can still lose some numeric precision because `float` has limited precision.

---

# 13. Type Conversion Process

The overall process can be remembered like this:

```text
        SOURCE VALUE
             ↓
        Source Data Type
             ↓
       Type Conversion
             ↓
     ┌───────┴────────┐
     ↓                ↓
 Widening          Narrowing
     ↓                ↓
Automatic          Explicit
     ↓                ↓
Small → Large     Large → Small
                       ↓
                 Possible Data Loss
```

### Example — Widening

```java
int number = 100;

double result = number;
```

Process:

```text
int
 ↓
double
 ↓
Automatic conversion
```

### Example — Narrowing

```java
double number = 100.75;

int result = (int) number;
```

Process:

```text
double
   ↓
(int)
   ↓
int
   ↓
100
```

`.75` is discarded.

---

