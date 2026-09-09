## Arrays:
An array is used to store multiple values of the same data type in one variable.

**Instead of:**
```
String browser1 = "Chrome";
String browser2 = "Edge";
String browser3 = "Firefox";
String browser4 = "Safari";
```

**We can use one array variable:**
```
String[] browsers = {"Chrome", "Edge", "Firefox", "Safari"};
```
**Intialization**
```
int a[] = new int[5]
```
### Types of arrays:

**1. One Dymentional arrays**
A one-dimensional array (1D array) in Java is a collection of multiple values of the same data type stored under one variable name, arranged in a single row/list.

**I. Basic 1D Array Operations**

| Operation        | What it means                    | Java example                        |
| ---------------- | -------------------------------- | ----------------------------------- |
| **Create**       | Create an array                  | `int[] numbers = new int[5];`       |
| **Initialize**   | Give values while creating       | `int[] numbers = {10,20,30,40,50};` |
| **Access**       | Read a value                     | `numbers[2]`                        |
| **Update**       | Change a value                   | `numbers[2] = 35;`                  |
| **Traverse**     | Visit every value                | `for` loop                          |
| **Search**       | Find a particular value          | `if (numbers[i] == 30)`             |
| **Count**        | Count values meeting a condition | `count++`                           |
| **Find maximum** | Find largest value               | Compare values                      |
| **Find minimum** | Find smallest value              | Compare values                      |
| **Sum**          | Add all values                   | `sum += numbers[i]`                 |
| **Average**      | Calculate average                | `sum / length`                      |
| **Sort**         | Arrange values                   | `Arrays.sort()`                     |
| **Reverse**      | Reverse the order                | Loop / swapping                     |
| **Copy**         | Copy an array                    | `Arrays.copyOf()`                   |

**II. Java Built in methods for Arrys**

- **Must Know:**
  
| **Method**              | **Use**                          | **Example**                         | **Result**             |
| ----------------------- | -------------------------------- | ----------------------------------- | ---------------------- |
| `Arrays.toString()`     | Convert array to readable String | `Arrays.toString(numbers)`          | `[50, 20, 40, 10, 30]` |
| `Arrays.sort()`         | Sort array ascending             | `Arrays.sort(numbers)`              | `[10, 20, 30, 40, 50]` |
| `Arrays.binarySearch()` | Search for a value               | `Arrays.binarySearch(numbers, 30)`  | Index of `30`          |
| `Arrays.equals()`       | Compare two arrays               | `Arrays.equals(a, b)`               | `true` / `false`       |
| `Arrays.copyOf()`       | Copy an array                    | `Arrays.copyOf(numbers, 3)`         | First 3 elements       |
| `Arrays.copyOfRange()`  | Copy a specific range            | `Arrays.copyOfRange(numbers, 1, 4)` | Elements index 1–3     |
| `Arrays.fill()`         | Fill array with same value       | `Arrays.fill(numbers, 0)`           | `[0,0,0,0,0]`          |
| `Arrays.asList()`       | Convert object array to List     | `Arrays.asList(names)`              | List representation    |
| `Arrays.mismatch()`     | Find first different position    | `Arrays.mismatch(a, b)`             | Index of difference    |

- **Learn Later**

| **Method**              | **Use**                              | **Example**                           | **Result**                |
| ----------------------- | ------------------------------------ | ------------------------------------- | ------------------------- |
| `Arrays.deepToString()` | Print multidimensional array         | `Arrays.deepToString(matrix)`         | Readable nested array     |
| `Arrays.deepEquals()`   | Compare multidimensional arrays      | `Arrays.deepEquals(a, b)`             | `true` / `false`          |
| `Arrays.compare()`      | Compare two arrays                   | `Arrays.compare(a, b)`                | Negative / `0` / positive |
| `Arrays.hashCode()`     | Generate array hash code             | `Arrays.hashCode(numbers)`            | Integer hash              |
| `Arrays.deepHashCode()` | Generate hash code for nested arrays | `Arrays.deepHashCode(matrix)`         | Integer hash              |
| `Arrays.stream()`       | Create Stream from array             | `Arrays.stream(numbers)`              | Stream                    |
| `Arrays.setAll()`       | Generate values using a function     | `Arrays.setAll(numbers, i -> i * 10)` | Generated values          |

- **Advanced:**

| **Method**                 | **Use**                            | **Example**                           | **Result**                |
| -------------------------- | ---------------------------------- | ------------------------------------- | ------------------------- |
| `Arrays.parallelSort()`    | Sort using parallel processing     | `Arrays.parallelSort(numbers)`        | Sorted array              |
| `Arrays.parallelSetAll()`  | Generate values in parallel        | `Arrays.parallelSetAll(numbers, ...)` | Generated values          |
| `Arrays.parallelPrefix()`  | Calculate cumulative/prefix values | `Arrays.parallelPrefix(numbers, ...)` | Prefix results            |
| `Arrays.compareUnsigned()` | Compare arrays as unsigned values  | `Arrays.compareUnsigned(a, b)`        | Negative / `0` / positive |

============================================================================================

**2. Two Dymentional arrays**

A two-dimensional array is an array where data is organized in rows and columns.
```
             Column
             0    1    2
           +----+----+----+
Row 0      | 10 | 20 | 30 |
           +----+----+----+
Row 1      | 40 | 50 | 60 |
           +----+----+----+
Row 2      | 70 | 80 | 90 |
           +----+----+----+
```

=================================================================================================

**How to Expect Input from User/keyboard**
``` JAVA

import java.util.Scanner;

public class UserInput {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");

        int number = sc.nextInt();

        System.out.println("You entered: " + number);
    }
}
```

| Java Data Type | Scanner Method           | Example Input | Variable Declaration            | Stored Value    |
| -------------- | ------------------------ | ------------- | ------------------------------- | --------------- |
| `byte`         | `nextByte()`             | `100`         | `byte x = sc.nextByte();`       | `100`           |
| `short`        | `nextShort()`            | `20000`       | `short x = sc.nextShort();`     | `20000`         |
| `int` ⭐        | `nextInt()`              | `500`         | `int x = sc.nextInt();`         | `500`           |
| `long`         | `nextLong()`             | `500000L`     | `long x = sc.nextLong();`       | `500000`        |
| `float`        | `nextFloat()`            | `25.5`        | `float x = sc.nextFloat();`     | `25.5`          |
| `double` ⭐     | `nextDouble()`           | `99.99`       | `double x = sc.nextDouble();`   | `99.99`         |
| `boolean`      | `nextBoolean()`          | `true`        | `boolean x = sc.nextBoolean();` | `true`          |
| `char`         | No direct `nextChar()` ❌ | `A`           | `char x = sc.next().charAt(0);` | `A`             |
| `String`       | `next()`                 | `Ramesh`      | `String x = sc.next();`         | `"Ramesh"`      |
| `String`       | `nextLine()` ⭐           | `Hello World` | `String x = sc.nextLine();`     | `"Hello World"` |


**How to accept input from user**

- Import Scanner
```
import java.util.Scanner;
```

- Create a Scanner object
```
Scanner sc = new Scanner(System.in);
```

- Read different types of input
```JAVA
import java.util.Scanner;

public class UserInput {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.print("Enter your salary: ");
        double salary = sc.nextDouble();

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Salary: " + salary);

        sc.close();
    }
}
```










