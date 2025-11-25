# Complete Java Guide for Absolute Beginners

## Table of Contents
1. [Introduction to Java](#introduction)
2. [Setting Up Your Environment](#setup)
3. [Understanding Your First Program](#first-program)
4. [Variables Deep Dive](#variables)
5. [Operators in Detail](#operators)
6. [Control Flow Statements](#control-flow)
7. [Loops Explained](#loops)
8. [Methods/Functions](#methods)
9. [Arrays](#arrays)
10. [Object-Oriented Programming Basics](#oop)

---

## 1. Introduction to Java {#introduction}

### What is Java?
Java is a **programming language** and a **computing platform**. Think of it like a language you use to give instructions to a computer.

### Why Learn Java?
- **Popular**: Used by millions of developers worldwide
- **Versatile**: Build apps for phones (Android), websites, desktop software, games
- **Good Salary**: Java developers are in high demand
- **Beginner-Friendly**: Clear syntax and strong community support

### How Java Works
```
You Write Code (.java file)
        ↓
Compiler converts it (javac command)
        ↓
Bytecode created (.class file)
        ↓
JVM (Java Virtual Machine) runs it
        ↓
Program Executes
```

---

## 2. Setting Up Your Environment {#setup}

### Step-by-Step Installation

#### Windows:
1. Go to https://www.oracle.com/java/technologies/downloads/
2. Download JDK (Java Development Kit) - latest version
3. Run the installer, click Next → Next → Install
4. Set Environment Variable:
   - Right-click "This PC" → Properties
   - Advanced System Settings → Environment Variables
   - Under System Variables, find "Path" → Edit
   - Add: `C:\Program Files\Java\jdk-XX\bin` (replace XX with version)

#### Verify Installation:
Open Command Prompt (cmd) and type:
```bash
java -version
javac -version
```
You should see version numbers. If yes, you're ready!

### IDE (Code Editor) Options
- **VS Code**: Lightweight, install "Extension Pack for Java"
- **IntelliJ IDEA**: Professional, beginner-friendly
- **Eclipse**: Free, powerful
- **Notepad++**: Simple text editor

---

## 3. Understanding Your First Program {#first-program}

### The Classic "Hello World"

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Breaking It Down Line by Line

#### Line 1: `public class HelloWorld {`
- **public**: Anyone can access this class (don't worry about this yet)
- **class**: Everything in Java lives inside a class (like a container)
- **HelloWorld**: The name of your class (MUST match filename)
- **{**: Opening brace - everything inside belongs to this class

#### Line 2: `public static void main(String[] args) {`
This is the **main method** - the starting point of every Java program.

- **public**: Accessible from anywhere
- **static**: Can run without creating an object (advanced topic)
- **void**: This method doesn't return any value
- **main**: Special name Java looks for to start the program
- **String[] args**: Can accept text input from command line (optional)

#### Line 3: `System.out.println("Hello, World!");`
- **System**: A built-in Java class
- **out**: Output stream (where text goes - your screen)
- **println**: Print line - displays text and moves to next line
- **"Hello, World!"**: The text to display (must be in quotes)
- **;**: Every statement in Java ends with semicolon

#### Lines 4-5: `} }`
Closing braces for the method and class

### How to Run It

**Step 1: Create the file**
- Open Notepad or your IDE
- Type the code exactly as shown
- Save as `HelloWorld.java` (name must match class name!)

**Step 2: Compile**
```bash
javac HelloWorld.java
```
This creates `HelloWorld.class` (bytecode file)

**Step 3: Run**
```bash
java HelloWorld
```
Output: `Hello, World!`

### Common Errors
❌ **Class name doesn't match filename**: Error!
❌ **Missing semicolon**: Compilation error
❌ **Wrong capitalization**: Java is case-sensitive

---

## 4. Variables Deep Dive {#variables}

### What is a Variable?
A variable is like a **labeled box** that stores data. You can put things in, take them out, or change them.

```java
int age = 25;
```
- `int` = type of box (stores whole numbers)
- `age` = name of the box (you choose this)
- `=` = assignment operator (puts value in box)
- `25` = the value stored
- `;` = end of statement

### Primitive Data Types

#### 1. **int** (Integer - Whole Numbers)
```java
int age = 25;
int year = 2025;
int temperature = -5;
int score = 0;

System.out.println("Age: " + age);  // Output: Age: 25
```
- **Range**: -2,147,483,648 to 2,147,483,647
- **Uses**: Counting, ages, years, scores

#### 2. **double** (Decimal Numbers)
```java
double price = 99.99;
double pi = 3.14159;
double temperature = 36.6;
double distance = 125.75;

System.out.println("Price: $" + price);  // Output: Price: $99.99
```
- **Range**: Very large, can have decimals
- **Uses**: Money, measurements, scientific calculations

#### 3. **char** (Single Character)
```java
char grade = 'A';
char initial = 'H';
char symbol = '@';

System.out.println("Grade: " + grade);  // Output: Grade: A
```
- **Important**: Use **single quotes** `' '`
- **Stores**: One character only

#### 4. **boolean** (True or False)
```java
boolean isRaining = true;
boolean isSunny = false;
boolean hasLicense = true;

System.out.println("Is it raining? " + isRaining);  // Output: Is it raining? true
```
- **Only two values**: `true` or `false`
- **Uses**: Conditions, yes/no situations

#### 5. **String** (Text/Words)
```java
String name = "Hariharan";
String city = "Chennai";
String message = "Welcome to Java!";

System.out.println("Hello, " + name);  // Output: Hello, Hariharan
```
- **Important**: Use **double quotes** `" "`
- **Not primitive**: It's a class (advanced topic)
- **Can be empty**: `String empty = "";`

### More Data Types

#### 6. **byte** (Small Numbers)
```java
byte age = 25;       // Range: -128 to 127
byte level = 100;
```

#### 7. **short** (Medium Numbers)
```java
short year = 2025;   // Range: -32,768 to 32,767
```

#### 8. **long** (Very Large Numbers)
```java
long population = 8000000000L;  // Note the 'L' at end
long distance = 9460730472580800L;
```

#### 9. **float** (Decimal, Less Precise)
```java
float temperature = 36.6f;  // Note the 'f' at end
```

### Variable Rules

✅ **Valid Names:**
```java
int age;
int studentAge;
int student_age;
int age2;
int $price;
```

❌ **Invalid Names:**
```java
int 2age;        // Can't start with number
int student-age; // No hyphens
int my age;      // No spaces
int class;       // Can't use reserved keywords
```

### Naming Conventions (Best Practices)
```java
int studentAge;      // camelCase - first word lowercase, rest capitalized
int numberOfStudents;
String firstName;
boolean isActive;
```

### Example Program with Multiple Variables

```java
public class StudentInfo {
    public static void main(String[] args) {
        // Student information
        String name = "Hariharan";
        int age = 22;
        char grade = 'A';
        double gpa = 3.85;
        boolean isEnrolled = true;
        
        // Display information
        System.out.println("=== Student Details ===");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Grade: " + grade);
        System.out.println("GPA: " + gpa);
        System.out.println("Enrolled: " + isEnrolled);
    }
}
```

**Output:**
```
=== Student Details ===
Name: Hariharan
Age: 22
Grade: A
GPA: 3.85
Enrolled: true
```

---

## 5. Operators in Detail {#operators}

### Arithmetic Operators (Math)

```java
public class ArithmeticDemo {
    public static void main(String[] args) {
        int a = 20;
        int b = 5;
        
        // Addition
        int sum = a + b;
        System.out.println("Addition: " + a + " + " + b + " = " + sum);
        // Output: Addition: 20 + 5 = 25
        
        // Subtraction
        int difference = a - b;
        System.out.println("Subtraction: " + a + " - " + b + " = " + difference);
        // Output: Subtraction: 20 - 5 = 15
        
        // Multiplication
        int product = a * b;
        System.out.println("Multiplication: " + a + " * " + b + " = " + product);
        // Output: Multiplication: 20 * 5 = 100
        
        // Division
        int quotient = a / b;
        System.out.println("Division: " + a + " / " + b + " = " + quotient);
        // Output: Division: 20 / 5 = 4
        
        // Modulus (Remainder)
        int remainder = a % b;
        System.out.println("Remainder: " + a + " % " + b + " = " + remainder);
        // Output: Remainder: 20 % 5 = 0
    }
}
```

### Special Division Cases

```java
// Integer division
int result1 = 10 / 3;     // result1 = 3 (not 3.33!)
System.out.println(result1);

// To get decimals, use double
double result2 = 10.0 / 3.0;  // result2 = 3.333...
System.out.println(result2);

// Modulus examples
System.out.println(10 % 3);   // 1 (10 ÷ 3 = 3 remainder 1)
System.out.println(15 % 4);   // 3 (15 ÷ 4 = 3 remainder 3)
System.out.println(20 % 5);   // 0 (20 ÷ 5 = 4 remainder 0)
```

### Increment and Decrement

```java
int count = 5;

// Increment (add 1)
count++;            // count = 6
count = count + 1;  // Same as above

// Decrement (subtract 1)
count--;            // count = 5
count = count - 1;  // Same as above

// Pre vs Post increment
int a = 5;
int b = a++;  // b = 5, then a becomes 6
int c = ++a;  // a becomes 7, then c = 7
```

### Comparison Operators (Compare Values)

```java
int x = 10;
int y = 5;

System.out.println(x == y);  // false (equal to?)
System.out.println(x != y);  // true  (not equal to?)
System.out.println(x > y);   // true  (greater than?)
System.out.println(x < y);   // false (less than?)
System.out.println(x >= y);  // true  (greater than or equal?)
System.out.println(x <= y);  // false (less than or equal?)
```

### Logical Operators (Combine Conditions)

```java
boolean hasLicense = true;
boolean hasInsurance = true;
int age = 20;

// AND (&&) - Both must be true
boolean canDrive = hasLicense && hasInsurance;
System.out.println(canDrive);  // true

boolean condition1 = (age > 18) && (age < 60);
System.out.println(condition1);  // true (age is between 18 and 60)

// OR (||) - At least one must be true
boolean isWeekend = true;
boolean isHoliday = false;
boolean canRest = isWeekend || isHoliday;
System.out.println(canRest);  // true

// NOT (!) - Reverses the value
boolean isRaining = false;
boolean isSunny = !isRaining;
System.out.println(isSunny);  // true
```

### Assignment Operators

```java
int num = 10;

num += 5;   // num = num + 5;  (num is now 15)
num -= 3;   // num = num - 3;  (num is now 12)
num *= 2;   // num = num * 2;  (num is now 24)
num /= 4;   // num = num / 4;  (num is now 6)
num %= 4;   // num = num % 4;  (num is now 2)
```

---

## 6. Control Flow Statements {#control-flow}

### If Statement (Make Decisions)

```java
public class IfDemo {
    public static void main(String[] args) {
        int age = 18;
        
        if (age >= 18) {
            System.out.println("You are an adult");
            System.out.println("You can vote");
        }
        
        System.out.println("Program continues...");
    }
}
```

**How it works:**
1. Check if condition `(age >= 18)` is true
2. If YES → Execute code inside `{ }`
3. If NO → Skip the code inside `{ }`

### If-Else (Two Options)

```java
public class IfElseDemo {
    public static void main(String[] args) {
        int marks = 65;
        
        if (marks >= 60) {
            System.out.println("PASSED!");
        } else {
            System.out.println("FAILED!");
        }
    }
}
```

**Flowchart:**
```
Check: marks >= 60?
    ↓
   YES → Print "PASSED!"
    ↓
   NO → Print "FAILED!"
```

### If-Else If-Else (Multiple Conditions)

```java
public class GradeCalculator {
    public static void main(String[] args) {
        int marks = 85;
        
        if (marks >= 90) {
            System.out.println("Grade: A+ (Excellent!)");
        } else if (marks >= 80) {
            System.out.println("Grade: A (Very Good!)");
        } else if (marks >= 70) {
            System.out.println("Grade: B (Good)");
        } else if (marks >= 60) {
            System.out.println("Grade: C (Average)");
        } else if (marks >= 50) {
            System.out.println("Grade: D (Below Average)");
        } else {
            System.out.println("Grade: F (Failed)");
        }
    }
}
```

**Important:** Java checks conditions **from top to bottom** and stops at the first TRUE condition.

### Nested If (If Inside If)

```java
public class NestedIfDemo {
    public static void main(String[] args) {
        int age = 25;
        boolean hasLicense = true;
        
        if (age >= 18) {
            System.out.println("Age requirement met");
            
            if (hasLicense) {
                System.out.println("You can drive!");
            } else {
                System.out.println("Get a license first");
            }
        } else {
            System.out.println("You're too young to drive");
        }
    }
}
```

### Switch Statement (Multiple Fixed Options)

```java
public class SwitchDemo {
    public static void main(String[] args) {
        int day = 3;
        
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
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            case 7:
                System.out.println("Sunday");
                break;
            default:
                System.out.println("Invalid day");
        }
    }
}
```

**Important:** Always use `break;` or it will "fall through" to next case!

---

## 7. Loops Explained {#loops}

### What is a Loop?
A loop repeats code multiple times. Like doing push-ups - you repeat the same action.

### For Loop (Know How Many Times)

#### Basic Structure
```java
for (initialization; condition; update) {
    // Code to repeat
}
```

#### Example 1: Print 1 to 5
```java
public class ForLoopDemo {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Number: " + i);
        }
    }
}
```

**Step-by-step execution:**
```
Step 1: i = 1, Check i <= 5? YES → Print "Number: 1"
Step 2: i = 2, Check i <= 5? YES → Print "Number: 2"
Step 3: i = 3, Check i <= 5? YES → Print "Number: 3"
Step 4: i = 4, Check i <= 5? YES → Print "Number: 4"
Step 5: i = 5, Check i <= 5? YES → Print "Number: 5"
Step 6: i = 6, Check i <= 5? NO → Stop
```

#### Example 2: Multiplication Table
```java
public class MultiplicationTable {
    public static void main(String[] args) {
        int number = 7;
        
        System.out.println("Multiplication Table of " + number);
        System.out.println("============================");
        
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + (number * i));
        }
    }
}
```

**Output:**
```
Multiplication Table of 7
============================
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
...
7 x 10 = 70
```

#### Example 3: Sum of Numbers
```java
public class SumNumbers {
    public static void main(String[] args) {
        int sum = 0;
        
        for (int i = 1; i <= 100; i++) {
            sum = sum + i;  // or sum += i;
        }
        
        System.out.println("Sum of 1 to 100 = " + sum);  // 5050
    }
}
```

### While Loop (Repeat While Condition is True)

```java
public class WhileLoopDemo {
    public static void main(String[] args) {
        int count = 1;
        
        while (count <= 5) {
            System.out.println("Count: " + count);
            count++;  // IMPORTANT: Don't forget to update!
        }
    }
}
```

**Warning:** If you forget `count++`, the loop runs FOREVER (infinite loop)!

#### Example: Password Checker
```java
import java.util.Scanner;

public class PasswordChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String correctPassword = "java123";
        String enteredPassword = "";
        
        while (!enteredPassword.equals(correctPassword)) {
            System.out.print("Enter password: ");
            enteredPassword = scanner.nextLine();
            
            if (!enteredPassword.equals(correctPassword)) {
                System.out.println("Wrong password! Try again.");
            }
        }
        
        System.out.println("Access Granted!");
        scanner.close();
    }
}
```

### Do-While Loop (Execute At Least Once)

```java
public class DoWhileDemo {
    public static void main(String[] args) {
        int num = 1;
        
        do {
            System.out.println("Number: " + num);
            num++;
        } while (num <= 5);
    }
}
```

**Difference from while:**
- `while`: Check condition FIRST, then execute
- `do-while`: Execute FIRST, then check condition

```java
// This while loop won't run at all
int x = 10;
while (x < 5) {
    System.out.println("This never prints");
}

// This do-while runs once
int y = 10;
do {
    System.out.println("This prints once!");
} while (y < 5);
```

### Break and Continue

#### Break (Exit Loop Early)
```java
public class BreakDemo {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            if (i == 5) {
                break;  // Stop loop when i is 5
            }
            System.out.println(i);
        }
        // Output: 1 2 3 4
    }
}
```

#### Continue (Skip Current Iteration)
```java
public class ContinueDemo {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            if (i % 2 == 0) {
                continue;  // Skip even numbers
            }
            System.out.println(i);
        }
        // Output: 1 3 5 7 9 (only odd numbers)
    }
}
```

### Nested Loops (Loop Inside Loop)

```java
public class NestedLoopDemo {
    public static void main(String[] args) {
        // Print a pattern
        for (int row = 1; row <= 5; row++) {
            for (int col = 1; col <= row; col++) {
                System.out.print("* ");
            }
            System.out.println();  // New line after each row
        }
    }
}
```

**Output:**
```
* 
* * 
* * * 
* * * * 
* * * * * 
```

---

## 8. Methods/Functions {#methods}

### What is a Method?
A method is a **reusable block of code** that performs a specific task. Like a recipe you can use multiple times.

### Basic Method Structure

```java
public class MethodDemo {
    // Method definition
    public static void greet() {
        System.out.println("Hello!");
        System.out.println("Welcome to Java");
    }
    
    // Main method - program starts here
    public static void main(String[] args) {
        greet();  // Method call
        greet();  // Call it again
        greet();  // And again!
    }
}
```

**Output:**
```
Hello!
Welcome to Java
Hello!
Welcome to Java
Hello!
Welcome to Java
```

### Methods with Parameters (Input)

```java
public class ParameterDemo {
    // Method that takes one parameter
    public static void greetPerson(String name) {
        System.out.println("Hello, " + name + "!");
    }
    
    public static void main(String[] args) {
        greetPerson("Hariharan");  // Output: Hello, Hariharan!
        greetPerson("Raj");        // Output: Hello, Raj!
        greetPerson("Priya");      // Output: Hello, Priya!
    }
}
```

#### Multiple Parameters
```java
public class MultipleParameters {
    public static void addNumbers(int a, int b) {
        int sum = a + b;
        System.out.println(a + " + " + b + " = " + sum);
    }
    
    public static void main(String[] args) {
        addNumbers(5, 3);    // Output: 5 + 3 = 8
        addNumbers(10, 20);  // Output: 10 + 20 = 30
        addNumbers(7, 13);   // Output: 7 + 13 = 20
    }
}
```

### Methods with Return Values

```java
public class ReturnDemo {
    // Method that returns an integer
    public static int add(int a, int b) {
        int sum = a + b;
        return sum;  // Send back the result
    }
    
    public static void main(String[] args) {
        int result = add(5, 3);  // Store the returned value
        System.out.println("Result: " + result);  // Output: Result: 8
        
        // Use return value directly
        System.out.println("10 + 20 = " + add(10, 20));  // Output: 10 + 20 = 30
    }
}
```

### Real-World Example: Calculator

```java
public class Calculator {
    public static int add(int a, int b) {
        return a + b;
    }
    
    public static int subtract(int a, int b) {
        return a - b;
    }
    
    public static int multiply(int a, int b) {
        return a * b;
    }
    
    public static double divide(double a, double b) {
        return a / b;
    }
    
    public static void main(String[] args) {
        System.out.println("5 + 3 = " + add(5, 3));
        System.out.println("10 - 4 = " + subtract(10, 4));
        System.out.println("6 * 7 = " + multiply(6, 7));
        System.out.println("15 / 3 = " + divide(15, 3));
    }
}
```

---

## 9. Arrays {#arrays}

### What is an Array?
An array is a **collection of similar items** stored together. Like a row of lockers, each with a number.

### Creating Arrays

```java
// Method 1: Declare then assign
int[] numbers = new int[5];  // Array of 5 integers
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

// Method 2: Declare and initialize together
int[] scores = {85, 90, 78, 92, 88};

String[] names = {"Hariharan", "Raj", "Priya", "Amit"};
```

**Important:** Arrays start at index 0!
```
Index:  0    1    2    3    4
Value: [10] [20] [30] [40] [50]
```

### Accessing Array Elements

```java
public class ArrayDemo {
    public static void main(String[] args) {
        int[] numbers = {10, 20, 30, 40, 50};
        
        System.out.println(numbers[0]);  // 10 (first element)
        System.out.println(numbers[2]);  // 30 (third element)
        System.out.println(numbers[4]);  // 50 (last element)
        
        // Modify an element
        numbers[1] = 25;
        System.out.println(numbers[1]);  // 25 (changed from 20)
        
        // Array length
        System.out.println("Array length: " + numbers.length);  // 5
    }
}
```

### Looping Through Arrays

```java
public class ArrayLoop {
    public static void main(String[] args) {
        String[] fruits = {"Apple", "Banana", "Mango", "Orange"};
        
        // Method 1: For loop
        System.out.println("Method 1: Using for loop");
        for (int i = 0; i < fruits.length; i++) {
            System.out.println(i + ": " + fruits[i]);
        }
        
        // Method 2: Enhanced for loop (easier!)
        System.out.println("\nMethod 2: Using enhanced for loop");
        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```

### Array Examples

#### Example 1: Find Maximum Number
```java
public class FindMax {
    public static void main(String[] args) {
        int[] numbers = {45, 23, 67, 12, 89, 34};
        int max = numbers[0];  // Assume first is largest
        
        for (int i = 1; i < numbers.length; i++) {
            if (numbers[i] > max) {
                max = numbers[i];
            }
        }
        
        System.out.println("Maximum number: " + max);  // 89
    }
}
```

#### Example 2: Calculate Average
```java
public class CalculateAverage {
    public static void main(String[] args) {
        int[] marks = {85, 90, 78, 92, 88};
        int sum = 0;
        
        for (int mark : marks) {
            sum += mark;
        }
        
        double average = (double) sum / marks.length;
        System.out.println("Average marks: " + average);  // 86.6
    }
}
```

---

## 10. Object-Oriented Programming Basics {#oop}

### What is OOP?
Object-Oriented Programming is a way to organize code around **objects** (things) rather than just functions.

Think of it like this:
- **Class**: Blueprint (like a house plan)
- **Object**: Actual thing built from blueprint (actual house)

### Creating a Class

```java
// Student.java
public class Student {
    // Attributes (properties)
    String name;
    int age;
    String course;
    double gpa;
    
    // Method (behavior)
    public void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Course: " + course);
        System.out.println("GPA: " + gpa);
    }
    
    public void study() {
        System.out.println(name + " is studying " + course);
    }
}
```

### Creating Objects

```java
// Main.java
public class Main {
    public static void main(String[] args) {
        // Create object (instance) of Student class
        Student student1 = new Student();
        student1.name = "Hariharan";
        student1.age = 22;
        student1.course = "Computer Science";
        student1.gpa = 3.85;
        
        // Create another object
        Student student2 = new Student();
        student2.name = "Priya";
        student2.age = 21;
        student2.course = "Engineering";
        student2.gpa = 3.92;
        
        // Use objects
        student1.displayInfo();
        System.out.println();
        student2.displayInfo();
        
        System.out.println();
        student1.study();
        student2.study();
    }
}
```

### Constructor (Special Method)

```java
public class Student {
    String name;
    int age;
    String course;
    
    // Constructor - runs when object is created
    public Student(String name, int age, String course) {
        this.name = name;
        this.age = age;
        this.course = course;
    }
    
    public void displayInfo() {
        System.out.println("Name: " + name + ", Age: " + age + ", Course: " + course);
    }
}

// Using constructor
public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("Hariharan", 22, "CS");
        Student s2 = new Student("Raj", 23, "IT");
        
        s1.displayInfo();
        s2.displayInfo();
    }
}
```

---

## Practice Exercises

### Exercise 1: Number Guessing Game
```java
import java.util.Scanner;

public class GuessingGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int secretNumber = 42;
        int guess = 0;
        int attempts = 0;
        
        System.out.println("Guess the number between 1 and 100!");
        
        while (guess != secretNumber) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            attempts++;
            
            if (guess < secretNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > secretNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Correct! You guessed it in " + attempts + " attempts!");
            }
        }
        
        scanner.close();
    }
}
```

### Exercise 2: Bank Account Class
```java
public class BankAccount {
    String accountHolder;
    double balance;
    
    public BankAccount(String name, double initialBalance) {
        accountHolder = name;
        balance = initialBalance;
    }
    
    public void deposit(double amount) {
        balance += amount;
        System.out.println("Deposited: $" + amount);
        showBalance();
    }
    
    public void withdraw(double amount) {
        if (amount > balance) {
            System.out.println("Insufficient funds!");
        } else {
            balance -= amount;
            System.out.println("Withdrawn: $" + amount);
            showBalance();
        }
    }
    
    public void showBalance() {
        System.out.println("Current Balance: $" + balance);
    }
    
    public static void main(String[] args) {
        BankAccount account = new BankAccount("Hariharan", 1000);
        account.showBalance();
        account.deposit(500);
        account.withdraw(300);
        account.withdraw(2000);  // Should fail
    }
}
```

---

## Learning Path

### Week 1-2: Basics
- ✅ Variables and data types
- ✅ Operators
- ✅ Input/Output
- ✅ If-else statements

### Week 3-4: Control Flow
- ✅ Loops (for, while, do-while)
- ✅ Switch statements
- ✅ Break and continue

### Week 5-6: Methods & Arrays
- ✅ Creating methods
- ✅ Parameters and return values
- ✅ Arrays and loops

### Week 7-8: OOP
- ✅ Classes and objects
- ✅ Constructors
- ✅ Methods in classes

### Next Topics (Advanced)
- Inheritance
- Polymorphism
- Exception handling
- File I/O
- Collections (ArrayList, HashMap)
- GUI programming

---

## Tips for Success

1. **Type, Don't Copy**: Type every example yourself
2. **Break Things**: Modify code to see what happens
3. **Practice Daily**: 30-60 minutes consistently
4. **Debug Errors**: Errors teach you the most
5. **Build Projects**: Apply what you learn
6. **Ask Questions**: No question is too basic
7. **Review Regularly**: Revisit concepts weekly

## Common Mistakes to Avoid

❌ **Missing semicolons**: Every statement needs `;`
❌ **Case sensitivity**: `String` vs `string`
❌ **Array index**: Arrays start at 0, not 1
❌ **Infinite loops**: Always update loop counter
❌ **Integer division**: `5 / 2` = 2, not 2.5
❌ **Comparing strings**: Use `.equals()` not `==`

---

## Resources

- **Official Documentation**: https://docs.oracle.com/javase/tutorial/
- **Practice**: HackerRank, LeetCode, Codewars
- **Videos**: YouTube - Programming with Mosh, freeCodeCamp
- **Books**: "Head First Java", "Java: A Beginner's Guide"

---

**You're now ready to start coding! Begin with the first program and work your way through. Good luck! 🚀**

