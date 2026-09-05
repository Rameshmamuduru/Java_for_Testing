## Controll_Statements:

a control statement is a statement that **controls the flow (order)** in which your program executes.

**Types**

**1. Conditional Statements/Decision / Selection**

**2. looping/iterative statements**
   
**4. jumping statements****

| Type                        | Purpose                        | Statements                           |
| --------------------------- | ------------------------------ | ------------------------------------ |
| **1. Decision / Selection** | Choose what code to execute    | `if`, `if-else`, `else-if`, `switch` |
| **2. Loop / Iteration**     | Repeat code                    | `for`, `while`, `do-while`           |
| **3. Jump / Branching**     | Change or exit the normal flow | `break`, `continue`, `return`        |

============================================================================================


### 1. Conditional Statements/Decision/Selection:
Decision statements allow a Java program to make a **decision based on a condition.**
```
User enters username and password
             ↓
       Are credentials valid?
          ↙        ↘
       YES          NO
        ↓            ↓
 Login Success   Login Failed
```
- Conditional Statements/Decision/Selection:
  - if
  - if else
  - nested if
  - else if ladder
  - swich

### if Condition:
```
if (condition) {
    // code to execute
}
```
```
int age = 15;

if (age >= 18) {
    System.out.println("Eligible to vote");
}
```
**If Condiction is False no ouput**

### If Else Condition:
```
if (condition) {
    // true block
} else {
    // false block
}
```

```
int age = 16;

if (age >= 18) {
    System.out.println("Eligible");
} else {
    System.out.println("Not Eligible");
}
```

### else-if Ladder:
```
int marks = 85;

if (marks >= 90) {
    System.out.println("Grade A");
} else if (marks >= 75) {
    System.out.println("Grade B");
} else if (marks >= 60) {
    System.out.println("Grade C");
} else if (marks >= 40) {
    System.out.println("Grade D");
} else {
    System.out.println("Fail");
}
```
### nested IF:
```
int age = 25;
boolean hasLicense = true;

if (age >= 18) {

    if (hasLicense) {
        System.out.println("Can drive");
    }

}
```
- Nested if with else
```
String username = "admin";
String password = "wrong";

if (username.equals("admin")) {

    if (password.equals("admin123")) {
        System.out.println("Login Successful");
    } else {
        System.out.println("Invalid Password");
    }

} else {
    System.out.println("Invalid Username");
}
```

### Switch:
```
int day = 2;

switch (day) {

    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    case 3:
        System.out.println("Wednesday");
        break;

    default:
        System.out.println("Invalid day");
}
```
============================================================================================


## 2. Looping statements:
A loop allows Java to execute the **same block of code repeatedly as long as a condition is satisfied.**

### Types of loops in Java:

| Loop         | Best used when                                           |
| ------------ | -------------------------------------------------------- |
| **for**      | You know how many times you want to repeat               |
| **while**    | You repeat while a condition remains true                |
| **do-while** | You want the code to execute at least once               |
| **for-each** | You want to process every element in an array/collection |

### for loop:
```
for (initialization; condition; update) {
    // code
}

Example:

for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### while loop:
```
while (condition) {
    // code
}
```
```
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

### do-while loop:

```
do {
    // code
} while (condition);
```

```
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

### for-each loop:
This is extremely useful when working with arrays and collections.
```
String[] browsers = {"Chrome", "Edge", "Firefox"};
```

```
for (String browser : browsers) {
    System.out.println(browser);
}
```
============================================================================================

## 3. Jumping Statements:

### break: 
Immediately stop the loop.
```
for (int i = 1; i <= 10; i++) {

    if (i == 5) {
        break;
    }

    System.out.println(i);
}
```
### continue:
Skip the current iteration and move to the next iteration.
```
for (int i = 1; i <= 5; i++) {

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
```


## Practice:

**Beginner**

- Print numbers 1–10.
- Print numbers 10–1.
- Print even numbers 1–20.
- Print odd numbers 1–20.
- Print multiples of 5 up to 50.
  
**Intermediate**

- Calculate the sum of numbers 1–10.
- Calculate the multiplication table of a number.
- Count how many numbers from 1–100 are divisible by 5.
- Find the largest of several numbers using a loop.
- Reverse a number.
  
**Automation-oriented**
  
- Loop through 5 usernames and print each.
- Loop through 5 products and print their names.
- Loop through product prices and calculate the total.
- Search a list of products and use break when the desired product is found.
- Loop through test data and identify which test cases passed/failed.









