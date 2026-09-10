## Problems:

|  # | Problem                    | Status      |
| -: | -------------------------- | ----------- |
|  1 | Print elements             | ✅           |
|  2 | Reverse array              | ✅/Practiced |
|  3 | Sum                        | ✅           |
|  4 | Largest element            | —           |
|  5 | Smallest element           | —           |
|  6 | Count even/odd             | —           |
|  7 | Search element             | —           |
|  8 | Second largest             | —           |
|  9 | Count occurrences          | ✅           |
| 10 | Find duplicates            | ✅           |
| 11 | Remove duplicates          | ✅           |
| 12 | Bubble Sort                | Practiced   |
| 13 | Move zeros to end          | —           |
| 14 | Pair with target sum       | —           |
| 15 | Compare expected vs actual | —           |


## Array methods:

**1. Must Master**

| Method                  | Description                                                         | Common Testing Use Case                                      | General Structure                     |
| ----------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------- |
| `Arrays.toString()`     | Converts a 1D array into a readable `String`                        | Print/log **expected and actual** array values for debugging | `Arrays.toString(array)`              |
| `Arrays.sort()`         | Sorts array elements in **ascending order**                         | Sort test data before comparison or verification             | `Arrays.sort(array)`                  |
| `Arrays.equals()`       | Compares two arrays element-by-element; **order matters**           | Compare **expected vs actual** array results                 | `Arrays.equals(array1, array2)`       |
| `Arrays.copyOf()`       | Creates a **new array** by copying an existing array                | Create a separate copy of test data or change array size     | `Arrays.copyOf(array, newLength)`     |
| `Arrays.copyOfRange()`  | Creates a new array containing a **specific range**                 | Extract/compare a particular portion of test data            | `Arrays.copyOfRange(array, from, to)` |
| `Arrays.fill()`         | Fills all or part of an array with the **same value**               | Initialize/reset test-data arrays                            | `Arrays.fill(array, value)`           |
| `Arrays.binarySearch()` | Searches for an element in a **sorted array** and returns its index | Quickly verify whether a value exists in sorted test data    | `Arrays.binarySearch(array, value)`   |


**2. Useful to Know**

| Method                  | Description                                        | Common Use Case                                       | General Structure                   |
| ----------------------- | -------------------------------------------------- | ----------------------------------------------------- | ----------------------------------- |
| `Arrays.deepToString()` | Converts multidimensional array to readable String | Display 2D/3D test data                               | `Arrays.deepToString(array)`        |
| `Arrays.deepEquals()`   | Compares multidimensional arrays                   | Compare expected vs actual 2D data                    | `Arrays.deepEquals(array1, array2)` |
| `Arrays.compare()`      | Compares two arrays lexicographically              | Compare array contents/order                          | `Arrays.compare(array1, array2)`    |
| `Arrays.mismatch()`     | Finds the first index where two arrays differ      | Identify the first difference between expected/actual | `Arrays.mismatch(array1, array2)`   |
| `Arrays.hashCode()`     | Generates a hash code based on array contents      | Hash-based comparison/storage                         | `Arrays.hashCode(array)`            |
| `Arrays.asList()`       | Converts an array to a `List`                      | Working between arrays and collections                | `Arrays.asList(array)`              |
| `Arrays.parallelSort()` | Sorts an array using parallel processing           | Large arrays                                          | `Arrays.parallelSort(array)`        |

