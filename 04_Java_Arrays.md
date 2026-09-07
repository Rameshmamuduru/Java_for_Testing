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

**1. Single Dymentional arrays**
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

| Method                  | Use                              | Example                             | Result                 |
| ----------------------- | -------------------------------- | ----------------------------------- | ---------------------- |
| `Arrays.toString()`     | Convert array to readable String | `Arrays.toString(numbers)`          | `[50, 20, 40, 10, 30]` |
| `Arrays.sort()`         | Sort array ascending             | `Arrays.sort(numbers)`              | `[10, 20, 30, 40, 50]` |
| `Arrays.binarySearch()` | Search for a value               | `Arrays.binarySearch(numbers, 30)`  | Index of `30`          |
| `Arrays.equals()`       | Compare two arrays               | `Arrays.equals(a, b)`               | `true` / `false`       |
| `Arrays.copyOf()`       | Copy an array                    | `Arrays.copyOf(numbers, 3)`         | First 3 elements       |
| `Arrays.copyOfRange()`  | Copy a specific range            | `Arrays.copyOfRange(numbers, 1, 4)` | Elements index 1–3     |
| `Arrays.fill()`         | Fill array with same value       | `Arrays.fill(numbers, 0)`           | `[0,0,0,0,0]`          |
| `Arrays.asList()`       | Convert array to List*           | `Arrays.asList(names)`              | List representation    |
| `Arrays.mismatch()`     | Find first different position    | `Arrays.mismatch(a,b)`              | Index of difference    |






