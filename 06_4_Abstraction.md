## Abstraction:
This is a process of hiding implementation details and showing only the essential functionality to the user. To achieve the Abstraction, we have 

**1. Interface**

- This is blueprint of the class.
- this contains final and static variables. (By default Final and Static variables)
- contains abstract methods (un-implemented methods), Static and default will be allowed but not the normal methods like in classes.
- Abstract methods consists of only signeture not the implementation.
- support the multiple inheritence.

<img width="703" height="197" alt="image" src="https://github.com/user-attachments/assets/06c9b1c1-bafc-4753-897e-8643d23e1c67" />

**Example**

```JAVA
import java.awt.*; 
import javax.swing.*; 


interface Shape {
    int length=10;
    int width=20;

    void circle();

    default void square() {
        System.out.println("this is a square");
    }

    static void rectangle() {
        System.out.println("this is a rectangle");
    }

}

public class HelloWorld implements Shape {
    public void circle() {
        System.out.println("this is a circle");
    }

    void Triangle() {
         System.out.println("this is a Triangle");
    }

    public static void main (String[] args) {

        // Scenaroi 1
        
        HelloWorld h = new HelloWorld();
        h.circle();
        h.square();
        Shape.rectangle();
        h.Triangle();
        System.out.println(h.length*h.width);
        System.out.println(Shape.length*Shape.width);

        // Scenaroi 2
        Shape s = new HelloWorld();
        s.circle();
        s.square();
        Shape.rectangle();
        // s.Triangle(); //this will not work
        System.out.println(s.length*s.width);
        System.out.println(Shape.length*Shape.width);
        
    }

}
```


**2. Abstract class**
