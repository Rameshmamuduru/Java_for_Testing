## Java Inheritance — Clear Notes

### 1. Definition

**Inheritance** is a mechanism in Java where a child class acquires the properties and methods of a parent class.

Keyword:

```java
extends
```

### Basic Syntax

```java
class Parent {
    // properties and methods
}

class Child extends Parent {
    // child properties and methods
}
```

---

# 1. Single Inheritance

**One parent → One child**

```text
Parent
   ↓
 Child
```

### Example

```java
class Animal {

    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {

    public static void main(String[] args) {

        Dog d = new Dog();

        d.eat();   // inherited method
        d.bark();  // own method
    }
}
```

### Output

```text
Animal eats
Dog barks
```

---

# 2. Multilevel Inheritance

**Parent → Child → Grandchild**

```text
Animal
   ↓
 Dog
   ↓
 Puppy
```

### Example

```java
class Animal {

    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog barks");
    }
}

class Puppy extends Dog {

    void play() {
        System.out.println("Puppy plays");
    }
}

public class Main {

    public static void main(String[] args) {

        Puppy p = new Puppy();

        p.eat();   // Animal
        p.bark(); // Dog
        p.play();  // Puppy
    }
}
```

### Output

```text
Animal eats
Dog barks
Puppy plays
```

---

# 3. Hierarchical Inheritance

**One parent → Multiple children**

```text
          Animal
          /    \
         ↓      ↓
       Dog     Cat
```

### Example

```java
class Animal {

    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {

    void meow() {
        System.out.println("Cat meows");
    }
}

public class Main {

    public static void main(String[] args) {

        Dog d = new Dog();
        d.eat();
        d.bark();

        Cat c = new Cat();
        c.eat();
        c.meow();
    }
}
```

### Output

```text
Animal eats
Dog barks
Animal eats
Cat meows
```

---

# 4. Multiple Inheritance

**Multiple parents → One child**

```text
Parent1     Parent2
    \         /
     \       /
       Child
```

Java **does not support multiple inheritance using classes**.

```java
class A {
}

class B {
}

// ❌ Not allowed
class C extends A, B {
}
```

### Using Interfaces

Java supports multiple inheritance through interfaces.

```java
interface A {

    void methodA();
}

interface B {

    void methodB();
}

class C implements A, B {

    public void methodA() {
        System.out.println("A");
    }

    public void methodB() {
        System.out.println("B");
    }
}
```

```text
Interface A     Interface B
      \             /
       \           /
          Class C
```

---

# 5. Hybrid Inheritance

**Combination of two or more types of inheritance.**

Example:

```text
          Animal
          /    \
         Dog   Cat
          |
        Puppy
```

This combines:

* Hierarchical inheritance
* Multilevel inheritance

Java does **not support hybrid inheritance using classes alone**.

It can be achieved using **interfaces**.

---

# Summary

| Type             | Structure    | Java                           |
| ---------------- | ------------ | ------------------------------ |
| **Single**       | A → B        | ✅                              |
| **Multilevel**   | A → B → C    | ✅                              |
| **Hierarchical** | A → B, A → C | ✅                              |
| **Multiple**     | A + B → C    | ❌ Classes / ✅ Interfaces       |
| **Hybrid**       | Combination  | ❌ Classes alone / ✅ Interfaces |

## One-line memory

```text
Single       → One parent, one child
Multilevel   → Parent → Child → Grandchild
Hierarchical → One parent, multiple children
Multiple     → Multiple parents, one child
Hybrid       → Combination of inheritance types
```
