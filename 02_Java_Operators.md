## Operators:

1. **Arithmetic operators** → + - * / %
2. **Assignment operators** → = += -= *= /= %=
3. **Relational operators** → == != > < >= <=
4. **Logical operators** → && || !
5. **Unary operators** → ++ -- + - !
6. **Ternary operator** → condition ? value1 : value2
7. **Bitwise operators** → & | ^ ~ << >>

## 1. Arithmetic Operators in Java:
Arithmetic operators are used to perform mathematical calculations on values.

| Operator | Name              | Example  | Result |
| -------- | ----------------- | -------- | -----: |
| `+`      | Addition          | `10 + 5` |   `15` |
| `-`      | Subtraction       | `10 - 5` |    `5` |
| `*`      | Multiplication    | `10 * 5` |   `50` |
| `/`      | Division          | `10 / 5` |    `2` |
| `%`      | Modulus/Remainder | `10 % 3` |    `1` |

- Addition:
``` JAVA
int a = 10;
int b = 5;

int result = a + b;

System.out.println(result);
```
| Operator | Explanation / Rule                                                                                   | Simple Java Program                                                                                                                 | Use Case in Testing                                                                            |
| -------- | ---------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `+`      | **Addition** – adds two values.                                                                      | `int a = 10;`<br>`int b = 5;`<br>`int result = a + b;`<br>`System.out.println(result);`<br>**Output:** `15`                         | Calculate **total price**, e.g. product price + shipping charges.                              |
| `-`      | **Subtraction** – subtracts the right value from the left value.                                     | `int a = 10;`<br>`int b = 5;`<br>`int result = a - b;`<br>`System.out.println(result);`<br>**Output:** `5`                          | Calculate **discount**, remaining balance, stock quantity, etc.                                |
| `*`      | **Multiplication** – multiplies two values.                                                          | `int price = 100;`<br>`int quantity = 3;`<br>`int result = price * quantity;`<br>`System.out.println(result);`<br>**Output:** `300` | Calculate **subtotal** = product price × quantity.                                             |
| `/`      | **Division** – divides the left value by the right value. With `int`, the decimal part is discarded. | `int a = 10;`<br>`int b = 3;`<br>`int result = a / b;`<br>`System.out.println(result);`<br>**Output:** `3`                          | Verify **average**, installment amount, pagination calculations, percentage calculations, etc. |
| `%`      | **Modulus** – returns the **remainder** after division.                                              | `int a = 10;`<br>`int b = 3;`<br>`int result = a % b;`<br>`System.out.println(result);`<br>**Output:** `1`                          | Check **even/odd values**, remaining items, batch processing, pagination, etc.                 |

## Arithamatic Operator Precedence:

```
( ) → * / % → + -
```

## Assignment operators:
Assignment operators are used to assign a value to a variable or update the existing value of a variable.
```JAVA
variable = value;
```
### Mind Map Table:

| Operator | Explanation / Rule                                                                             | Simple Java Program                                                                          | Use Case in Testing                                                                 |
| -------- | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `=`      | **Simple assignment** – assigns the value on the right to the variable on the left.            | `int price = 500;`<br>`System.out.println(price);`<br>**Output:** `500`                      | Store **test data**, such as username, price, quantity, expected result, etc.       |
| `+=`     | **Add and assign** – adds a value to the existing variable. `a += b` → `a = a + b`             | `int total = 500;`<br>`total += 100;`<br>`System.out.println(total);`<br>**Output:** `600`   | Add **shipping charges, taxes, additional fees**, etc. to an expected total.        |
| `-=`     | **Subtract and assign** – subtracts a value from the existing variable. `a -= b` → `a = a - b` | `int total = 500;`<br>`total -= 100;`<br>`System.out.println(total);`<br>**Output:** `400`   | Apply **discounts**, reduce stock, or subtract refunds/charges.                     |
| `*=`     | **Multiply and assign** – multiplies the existing variable by a value. `a *= b` → `a = a * b`  | `int price = 500;`<br>`price *= 3;`<br>`System.out.println(price);`<br>**Output:** `1500`    | Calculate **price × quantity** when validating an e-commerce order.                 |
| `/=`     | **Divide and assign** – divides the existing variable by a value. `a /= b` → `a = a / b`       | `int amount = 1000;`<br>`amount /= 4;`<br>`System.out.println(amount);`<br>**Output:** `250` | Validate **average values, installment amounts, or equally divided quantities**.    |
| `%=`     | **Modulus and assign** – calculates the remainder and stores it back. `a %= b` → `a = a % b`   | `int items = 17;`<br>`items %= 5;`<br>`System.out.println(items);`<br>**Output:** `2`        | Validate **remaining items**, batch processing, pagination, or even/odd conditions. |


## Relational operators:

Relational operators are used to compare two values. The result is always a boolean: true or false

| Operator | Explanation / Rule                                                             | Simple Java Program                                                                   | Use Case in Testing                                                              |
| -------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `==`     | Checks whether two values are **equal**.                                       | `int a = 10;`<br>`int b = 10;`<br>`System.out.println(a == b);`<br>**Output:** `true` | Compare **actual vs expected** values.                                           |
| `!=`     | Checks whether two values are **not equal**.                                   | `int a = 10;`<br>`int b = 20;`<br>`System.out.println(a != b);`<br>**Output:** `true` | Verify that an incorrect value is **not accepted** or two values differ.         |
| `>`      | Checks whether the left value is **greater than** the right value.             | `int price = 500;`<br>`System.out.println(price > 400);`<br>**Output:** `true`        | Verify a value is **above a limit**, such as minimum order amount.               |
| `<`      | Checks whether the left value is **less than** the right value.                | `int age = 17;`<br>`System.out.println(age < 18);`<br>**Output:** `true`              | Validate **maximum limits**, such as age or quantity restrictions.               |
| `>=`     | Checks whether the left value is **greater than or equal to** the right value. | `int amount = 1000;`<br>`System.out.println(amount >= 1000);`<br>**Output:** `true`   | Verify a value meets a **minimum requirement**, such as minimum purchase amount. |
| `<=`     | Checks whether the left value is **less than or equal to** the right value.    | `int quantity = 5;`<br>`System.out.println(quantity <= 10);`<br>**Output:** `true`    | Verify a value does not exceed a **maximum allowed limit**.                      |


## Logical Operators:

| Operator | Explanation / Rule                                                                | Simple Java Program                                                                                           | Use Case in Testing                                                                       |                                                                              |   |                                 |                                                                               |
| -------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | - | ------------------------------- | ----------------------------------------------------------------------------- |
| `&&`     | **Logical AND** – returns `true` only when **both conditions are true**.          | `int age = 25;`<br>`boolean hasID = true;`<br>`System.out.println(age >= 18 && hasID);`<br>**Output:** `true` | Verify multiple conditions together, e.g. **valid username AND valid password**.          |                                                                              |   |                                 |                                                                               |
| `        |                                                                                   | `                                                                                                             | **Logical OR** – returns `true` when **at least one condition is true**.                  | `int age = 17;`<br>`boolean parent = true;`<br>`System.out.println(age >= 18 |   | parent);`<br>**Output:** `true` | Validate alternative conditions, e.g. **email OR mobile number** is provided. |
| `!`      | **Logical NOT** – reverses the boolean value. `true` → `false`, `false` → `true`. | `boolean loggedIn = false;`<br>`System.out.println(!loggedIn);`<br>**Output:** `true`                         | Verify negative conditions, e.g. user **is not logged in** or button **is not disabled**. |                                                                              |   |                                 |                                                                               |


## Unary Operators:

| Operator | Explanation / Rule                                                                                          | Simple Java Program                                                                                 | Use Case in Testing                                                                          |
| -------- | ----------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `++`     | **Increment** – increases the value by `1`.                                                                 | `int count = 5;`<br>`count++;`<br>`System.out.println(count);`<br>**Output:** `6`                   | Increase **test counters**, iteration numbers, retry counts, item quantities, etc.           |
| `--`     | **Decrement** – decreases the value by `1`.                                                                 | `int count = 5;`<br>`count--;`<br>`System.out.println(count);`<br>**Output:** `4`                   | Decrease **retry counts**, stock quantities, loop counters, etc.                             |
| `+`      | **Unary plus** – indicates a positive value. Usually has no effect because numbers are positive by default. | `int number = 10;`<br>`int result = +number;`<br>`System.out.println(result);`<br>**Output:** `10`  | Rare in automation; can be used when explicitly representing a **positive numeric value**.   |
| `-`      | **Unary minus** – changes the sign of a value.                                                              | `int number = 10;`<br>`int result = -number;`<br>`System.out.println(result);`<br>**Output:** `-10` | Useful when validating **negative values**, refunds, balances, or negative test data.        |
| `!`      | **Logical NOT** – reverses a boolean value: `true → false`, `false → true`.                                 | `boolean loggedIn = false;`<br>`System.out.println(!loggedIn);`<br>**Output:** `true`               | Verify negative conditions, such as **user is not logged in**, button is not disabled, etc.  |
| `~`      | **Bitwise NOT** – reverses every bit of an integer value.                                                   | `int a = 5;`<br>`int result = ~a;`<br>`System.out.println(result);`<br>**Output:** `-6`             | Rare in normal UI automation; mainly relevant when testing **bit-level/system-level logic**. |

## Ternary Operator:
The **ternary operator** is a short way of writing a simple `if-else` condition.

### Basic syntax

```text
condition ? value1 : value2
```

Meaning:

```text
condition
   ↓
 true  → value1
 false → value2
```

| Operator | Explanation / Rule                                                                                        | Simple Java Program                                                                                                         | Use Case in Testing                                                                     |
| -------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `?:`     | Checks a condition. If the condition is **true**, it returns `value1`; if **false**, it returns `value2`. | `int age = 20;`<br>`String result = age >= 18 ? "Adult" : "Minor";`<br>`System.out.println(result);`<br>**Output:** `Adult` | Quickly determine **PASS/FAIL**, valid/invalid status, eligible/ineligible status, etc. |

### Simple example

```java
int marks = 75;

String result = marks >= 50 ? "PASS" : "FAIL";

System.out.println(result);
```
