## What is string:
Collection of characters and it was pre-defined classs
```JAVA
String name = "Ramesh";
String name = new String("jhon");
```
**Methods**
``` TABLE
| Method                  | Purpose                             | Example                                     |
| ----------------------- | ----------------------------------- | ------------------------------------------- |
| `length()`              | Returns number of characters        | `"Java".length()` → `4`                     |
| `charAt()`              | Gets character at index             | `"Java".charAt(1)` → `a`                    |
| `equals()`              | Compares two strings                | `"Java".equals("Java")` → `true`            |
| `equalsIgnoreCase()`    | Compares ignoring case              | `"JAVA".equalsIgnoreCase("java")` → `true`  |
| `contains()`            | Checks whether text exists          | `"Java Selenium".contains("Selenium")`      |
| `startsWith()`          | Checks beginning                    | `"Java".startsWith("Ja")`                   |
| `endsWith()`            | Checks ending                       | `"Java".endsWith("va")`                     |
| `toUpperCase()`         | Converts to uppercase               | `"java".toUpperCase()`                      |
| `toLowerCase()`         | Converts to lowercase               | `"JAVA".toLowerCase()`                      |
| `trim()`                | Removes leading/trailing spaces     | `" Java ".trim()`                           |
| `strip()`               | Removes leading/trailing whitespace | `" Java ".strip()`                          |
| `substring()`           | Extracts part of string             | `"Automation".substring(0,4)`               |
| `indexOf()`             | Finds first position                | `"Java".indexOf("a")` → `1`                 |
| `lastIndexOf()`         | Finds last position                 | `"Java".lastIndexOf("a")` → `3`             |
| `replace()`             | Replaces characters/text            | `"Java".replace("a","o")`                   |
| `replaceAll()`          | Replaces using regex                | `"abc123".replaceAll("\\d","")`             |
| `replaceFirst()`        | Replaces first match                | `"Java Java".replaceFirst("Java","Python")` |
| `concat()`              | Joins strings                       | `"Java".concat(" Testing")`                 |
| `split()`               | Splits string into array            | `"A,B,C".split(",")`                        |
| `isEmpty()`             | Checks if length is 0               | `"".isEmpty()` → `true`                     |
| `isBlank()`             | Checks empty/whitespace             | `"   ".isBlank()` → `true`                  |
| `compareTo()`           | Lexicographically compares          | `"A".compareTo("B")`                        |
| `compareToIgnoreCase()` | Compares ignoring case              | `"java".compareToIgnoreCase("JAVA")`        |
| `matches()`             | Checks regex pattern                | `"123".matches("\\d+")`                     |
| `toCharArray()`         | Converts String → char array        | `"Java".toCharArray()`                      |
| `valueOf()`             | Converts value → String             | `String.valueOf(100)`                       |

```
