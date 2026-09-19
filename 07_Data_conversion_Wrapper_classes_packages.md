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









