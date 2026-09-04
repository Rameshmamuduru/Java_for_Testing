## Controll_Statements"

a control statement is a statement that **controls the flow (order)** in which your program executes.

**Types**
1. Conditional Statements/Decision / Selection
2. looping/iterative statements
3. jumping statements

| Type                        | Purpose                        | Statements                           |
| --------------------------- | ------------------------------ | ------------------------------------ |
| **1. Decision / Selection** | Choose what code to execute    | `if`, `if-else`, `else-if`, `switch` |
| **2. Loop / Iteration**     | Repeat code                    | `for`, `while`, `do-while`           |
| **3. Jump / Branching**     | Change or exit the normal flow | `break`, `continue`, `return`        |

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








