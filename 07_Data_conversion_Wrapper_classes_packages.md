**1. Wrapper Classes**

- A wrapper class is a Java class that represents a primitive data type as an object.

| Wrapper Class | Wrapper for Primitive |
| ------------- | --------------------- |
| `Byte`        | `byte`                |
| `Short`       | `short`               |
| `Integer`     | `int`                 |
| `Long`        | `long`                |
| `Float`       | `float`               |
| `Double`      | `double`              |
| `Character`   | `char`                |
| `Boolean`     | `boolean`             |

**Data Conversion**

Data conversion means changing a value from one data type to another data type.

**Types of conversion**

```
                 DATA CONVERSION
                       │
          ┌────────────┴────────────┐
          ↓                         ↓
   Primitive Conversion       Reference/Object
          │                    Conversion
          │
    ┌─────┴─────┐
    ↓           ↓
Widening     Narrowing
```

**AutoBoxing**

Which means changing values from Object type to primitive Types

```JAVA
int a = 30;
Integer b = a;
```

**UnBoxing**

Which means changing values from Primitive type to Object type

```JAVA
Integer a=10;
int b=a;
```

**1. String → Primitive**
```
String
  │
  ├──→ int
  ├──→ long
  ├──→ float
  ├──→ double
  ├──→ boolean
  └──→ char
```
**String --> Int**

``` JAVA
public class HelloWorld {

    public static void main(String[] args) {

        String number = "1000";

        int a = Integer.parseInt(number);

        System.out.println(a);
    }
}
```

**String --> Long**

``` JAVA
public class HelloWorld {

    public static void main(String[] args) {

        String number = "1000";

        Long a = Long.parseLong(number);

        System.out.println(a);
    }
}
```

**String --> Float**

``` JAVA
public class HelloWorld {

    public static void main(String[] args) {

        String number = "1000";

        float a = Float.parseFloat(number);

        System.out.println(a);
    }
}
```

**String --> Double**

``` JAVA
public class HelloWorld {

    public static void main(String[] args) {

        String number = "1000";

        double a = Double.parseDouble(number);

        System.out.println(a);
    }
}
```

**String --> Boolean**

```JAVA
String value = "true";

boolean result = Boolean.parseBoolean(value);

System.out.println(result);
```

**String --> Char**

- There is no "Charecter.parseCharecter()"

```JAVA
public class HelloWorld {

    public static void main(String[] args) {

        String name = "Ramesh";

        char a = name.charAt(5);

        System.out.println(a);
    }
}
```

| String     | Target Primitive | Conversion               |
| ---------- | ---------------- | ------------------------ |
| `"100"`    | `int`            | `Integer.parseInt()`     |
| `"100000"` | `long`           | `Long.parseLong()`       |
| `"10.5"`   | `float`          | `Float.parseFloat()`     |
| `"10.5"`   | `double`         | `Double.parseDouble()`   |
| `"true"`   | `boolean`        | `Boolean.parseBoolean()` |
| `"A"`      | `char`           | `charAt(0)`              |






























