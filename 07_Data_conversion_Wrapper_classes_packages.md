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

**Data Conversion**

| #  | Conversion                     | Example            | Importance for SDET |
| -- | ------------------------------ | ------------------ | ------------------- |
| 1  | **Primitive → Primitive**      | `int → double`     | ⭐⭐⭐             |
| 2  | **String → Primitive**         | `"100" → int`      | ⭐⭐⭐⭐⭐        |
| 3  | **String → Wrapper**           | `"100" → Integer`  | ⭐⭐⭐⭐          |
| 4  | **Primitive → String**         | `100 → "100"`      | ⭐⭐⭐⭐⭐        |
| 5  | **Primitive → Wrapper**        | `int → Integer`    | ⭐⭐⭐⭐          |
| 6  | **Wrapper → String**           | `Integer → "100"`  | ⭐⭐⭐⭐          |
| 7  | **Wrapper → Primitive**        | `Integer → int`    | ⭐⭐⭐⭐⭐       |
| 8  | **Wrapper → Wrapper**          | `Integer → Double` | ⭐⭐⭐            |
| 9  | **Object → Object**            | `Dog → Animal`     | ⭐⭐⭐⭐         |
| 10 | **Object → Primitive/Wrapper** | `Object → Integer` | ⭐⭐⭐            |
| 11 | **Primitive/Wrapper → Object** | `int → Object`     | ⭐⭐⭐            |


============================================================================================

**Primitive → Primitive**

**1. Widening Conversion**

Smaller compatible type → larger compatible type

```
byte → short → int → long → float → double
```

```JAVA
int a = 100;
double b = a;
```

**2. Narrowing Conversion**

Larger type → smaller type.

```JAVA
double a = 100.5
int b = (int) a;
```

```
             Primitive → Primitive
                     │
             ┌───────┴───────┐
             ↓               ↓
         Widening         Narrowing
             │               │
       smaller → larger   larger → smaller
             │               │
        automatic        explicit cast

```

============================================================================================

**1. String → Primitive**

This can be done using by **Wrapper Class methods**

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

============================================================================================

**2. String --> Wrapper Class**

Instead of:
```JAVA
int number = Integer.parseInt("100");
```
```JAVA
Integer number = Integer.valueOf("100");
Float number = Float.valueOf("100")
```
============================================================================================

**3. Primitive --> String**

This can be achieved by 3 ways
- 1. String.valueOf()
- 2. Integer.toString()
 
``` JAVA
int num = 1023;
String res = String.valueOf(num);
System.out.println(res);
```
============================================================================================







































