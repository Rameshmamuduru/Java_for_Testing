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










