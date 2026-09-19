## Exception:

it was an abnormal event event occurred during the programe execuition and intrumpts the normal flow of the programme.

**Types of catagories**

**1. Checked Exception**

A checked exception is an exception that the Java compiler checks at compile time.
                              **(OR)**
Java knows that a particular operation can cause an exception, so the compiler forces you to either handle that exception or declare that your method can throw it.

### Example:

```JAVA
import java.io.FileReader;

public class Test {
    public static void main(String[] args) {

        FileReader file = new FileReader("data.txt");

    }
}
```

This gives a compilation error because FileReader can throw a checked exception if file does not exists in the location. and we have two ways to solve it.

**1. Handle it using try-catch**

```JAVA
import java.io.FileReader;
import java.io.FileNotFoundException;

public class Test {
    public static void main(String[] args) {

        try {
            FileReader file = new FileReader("data.txt");
        }
        catch (FileNotFoundException e) {
            System.out.println("File not found");
        }
    }
}
```

**2. Declare it using throws**

Instead of handling the exception yourself, you can tell the caller: "This method may produce this exception."

```JAVA
import java.io.FileReader;
import java.io.FileNotFoundException;

public class Test {

    public static void main(String[] args) throws FileNotFoundException {

        FileReader file = new FileReader("data.txt");
    }
}
```


**3. un-checked exception**

an exception that is not checked by the compiler at compile time and occurs during program execution.

**Example-1**
```JAVA
public class HelloWorld {
    public static void main(String[] args) {

        int num1=10;
        int num2 =2;
        
        try {
        int result = num1/num2;
        System.out.println(result);
        }
        catch(ArithmeticException e){
            System.out.println("Number can not be divided by Zero");
        }

    }
}
```
**if we can not know that which exception does the programe/line gonna raise so we can use "(Exception e)"**

```JAVA
public class HelloWorld {
    public static void main(String[] args) {

        int num1=10;
        int num2 =2;
        
        try {
        int result = num1/num2;
        System.out.println(result);
        }
        catch(Exception e){
            System.out.println("Number can not be divided by Zero");
        }

    }
}
```
============================================================

**finally**

finally is a block that is executed after try and catch, whether an exception occurs or not.

**Basic Structure**

```JAVA
try {
    // risky code
}
catch (Exception e) {
    // handle exception
}
finally {
    // code that should execute afterward
}
```

**Example**

```JAVA
try {
    int result = 10 / 0;
    System.out.println(result);
}
catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
}
finally {
    System.out.println("Finally block executed");
}
```

**finally is mainly used for cleanup — things that should happen whether the test/action passes or fails.**

```JAVA
WebDriver driver = new ChromeDriver();

try {
    driver.get("https://example.com");

    // Test steps
}
catch (Exception e) {
    System.out.println("Test failed: " + e.getMessage());
}
finally {
    driver.quit();
}
```









