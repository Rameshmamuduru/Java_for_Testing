**Types Casting**

Is a process of converting one Data types to another.

**there are two important contexts:**
```
Type Casting
│
├── Primitive casting
│   ├── Widening  → automatic
│   └── Narrowing → explicit
│
└── Object/Reference casting
    ├── Upcasting   → Child → Parent
    └── Downcasting → Parent → Child
```

**Object/Reference casting**

```JAVA
class Animal {
        void eat() {
            System.out.println("Eating");
        }
}

class Dog extends Animal {
        void bark() {
            System.out.println("baring");
        }
}

public class HelloWorld {

    public static void main(String[] args) {

    }

}
```
**Normal Object Creation**
```JAVA
public class HelloWorld {

    public static void main(String[] args) {

        Animal a = new Animal();
        a.eat();
        // a.bark();

        System.out.println("end of line");

        Dog d = new Dog();
        d.eat();
        d.bark();        
    }

}
```
**Up Casting**

```JAVA
Animal c = new Dog();
c.eat();
// c.bark();
```

**Down Casting**

```JAVA
Animal t = new Dog();
Dog f = (Dog) t;
f.eat();
f.bark();
```






















