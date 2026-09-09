## predefined Java classes

### 1. `java.lang` — Core Java classes

This package is automatically imported.

| Class              | Purpose                                  |
| ------------------ | ---------------------------------------- |
| `Object`           | Root class of Java                       |
| `String`           | Work with text                           |
| `StringBuilder`    | Mutable string manipulation              |
| `StringBuffer`     | Thread-safe mutable string               |
| `System`           | System/console operations                |
| `Math`             | Mathematical operations                  |
| `Integer`          | Wrapper for `int`                        |
| `Double`           | Wrapper for `double`                     |
| `Float`            | Wrapper for `float`                      |
| `Long`             | Wrapper for `long`                       |
| `Short`            | Wrapper for `short`                      |
| `Byte`             | Wrapper for `byte`                       |
| `Character`        | Character operations                     |
| `Boolean`          | Wrapper for `boolean`                    |
| `Number`           | Parent class for numeric wrapper classes |
| `Exception`        | Base class for exceptions                |
| `RuntimeException` | Runtime exceptions                       |
| `Thread`           | Multithreading                           |

---

### 2. `java.util` — Collections and utilities

Very important for automation.

| Class           | Purpose                     |
| --------------- | --------------------------- |
| `Scanner`       | Read input                  |
| `ArrayList`     | Dynamic array/list          |
| `LinkedList`    | Linked list                 |
| `HashSet`       | Unique elements             |
| `LinkedHashSet` | Unique + insertion order    |
| `TreeSet`       | Unique + sorted             |
| `HashMap`       | Key-value pairs             |
| `LinkedHashMap` | Key-value + insertion order |
| `TreeMap`       | Sorted key-value pairs      |
| `Collections`   | Collection operations       |
| `Arrays`        | Array operations            |
| `Random`        | Generate random values      |
| `Properties`    | Key-value configuration     |
| `Optional`      | Represent optional values   |

---

### 3. `java.io` — File handling

Important for test data and file operations.

| Class              | Purpose                |
| ------------------ | ---------------------- |
| `File`             | Files/directories      |
| `FileReader`       | Read files             |
| `FileWriter`       | Write files            |
| `BufferedReader`   | Efficient text reading |
| `BufferedWriter`   | Efficient text writing |
| `FileInputStream`  | Read binary data       |
| `FileOutputStream` | Write binary data      |
| `PrintWriter`      | Write formatted text   |

---

### 4. `java.time` — Date and time

Very useful in automation.

| Class               | Purpose                |
| ------------------- | ---------------------- |
| `LocalDate`         | Date                   |
| `LocalTime`         | Time                   |
| `LocalDateTime`     | Date + time            |
| `ZonedDateTime`     | Date + time + timezone |
| `Instant`           | Point in time          |
| `Duration`          | Time-based difference  |
| `Period`            | Date-based difference  |
| `DateTimeFormatter` | Format dates           |

---

### 5. `java.sql` — Database connectivity

Important for **database testing**.

| Class               | Purpose                       |
| ------------------- | ----------------------------- |
| `DriverManager`     | Establish database connection |
| `Connection`        | Database connection           |
| `Statement`         | Execute SQL                   |
| `PreparedStatement` | Execute parameterized SQL     |
| `CallableStatement` | Call stored procedures        |
| `ResultSet`         | Store query results           |
| `SQLException`      | Database exception            |

---

### 6. `java.net` — Networking

| Class               | Purpose                   |
| ------------------- | ------------------------- |
| `URL`               | Represents URL            |
| `URI`               | Represents URI            |
| `HttpURLConnection` | HTTP connection           |
| `Socket`            | Network communication     |
| `ServerSocket`      | Server-side communication |

---

## ⭐ What you should learn first

For your **Java → Automation Testing** path, I would prioritize them like this:

```text
LEVEL 1 — Core Java
String
Object
System
Math
Integer
Double
Character

        ↓

LEVEL 2 — Collections
ArrayList
HashSet
HashMap
Arrays
Collections

        ↓

LEVEL 3 — Exception Handling
Exception
RuntimeException

        ↓

LEVEL 4 — File Handling
File
FileReader
FileWriter
BufferedReader
BufferedWriter

        ↓

LEVEL 5 — Date & Time
LocalDate
LocalDateTime
DateTimeFormatter

        ↓

LEVEL 6 — Database Testing
DriverManager
Connection
PreparedStatement
ResultSet

        ↓

LEVEL 7 — Automation Framework
Selenium classes
TestNG classes
Rest Assured classes
```

## Classes where object creation is commonly used

| Class               | Object creation example                                       | Where used             |
| ------------------- | ------------------------------------------------------------- | ---------------------- |
| `Scanner`           | `Scanner sc = new Scanner(System.in);`                        | User input             |
| `String`            | `String name = new String("Ramesh");`*                        | Text                   |
| `StringBuilder`     | `StringBuilder sb = new StringBuilder();`                     | String manipulation    |
| `ArrayList`         | `ArrayList<Integer> list = new ArrayList<>();`                | Collections            |
| `LinkedList`        | `LinkedList<String> list = new LinkedList<>();`               | Collections            |
| `HashSet`           | `HashSet<String> set = new HashSet<>();`                      | Unique values          |
| `TreeSet`           | `TreeSet<Integer> set = new TreeSet<>();`                     | Sorted unique values   |
| `HashMap`           | `HashMap<String, Integer> map = new HashMap<>();`             | Key-value data         |
| `LinkedHashMap`     | `LinkedHashMap<String, Integer> map = new LinkedHashMap<>();` | Ordered key-value data |
| `TreeMap`           | `TreeMap<String, Integer> map = new TreeMap<>();`             | Sorted key-value data  |
| `Random`            | `Random r = new Random();`                                    | Random test data       |
| `File`              | `File file = new File("data.txt");`                           | File handling          |
| `FileReader`        | `FileReader fr = new FileReader(file);`                       | Reading files          |
| `FileWriter`        | `FileWriter fw = new FileWriter(file);`                       | Writing files          |
| `BufferedReader`    | `BufferedReader br = new BufferedReader(fr);`                 | Reading text           |
| `LocalDate`         | `LocalDate date = LocalDate.now();`                           | Dates                  |
| `LocalDateTime`     | `LocalDateTime dt = LocalDateTime.now();`                     | Date + time            |
| `DateTimeFormatter` | `DateTimeFormatter f = ...`                                   | Date formatting        |
| `Exception`         | `Exception e`                                                 | Exception handling     |
| `Connection`        | `Connection con = ...`                                        | Database testing       |
| `PreparedStatement` | `PreparedStatement ps = ...`                                  | SQL testing            |
| `ResultSet`         | `ResultSet rs = ...`                                          | Database results       |

### For your Automation Testing learning
```
1. Scanner
       ↓
2. String
       ↓
3. StringBuilder
       ↓
4. ArrayList
       ↓
5. HashSet
       ↓
6. HashMap
       ↓
7. Arrays / Collections
       ↓
8. File / BufferedReader
       ↓
9. LocalDate / LocalDateTime
       ↓
10. Database classes
       ↓
11. Selenium classes
       ↓
12. TestNG classes
```
