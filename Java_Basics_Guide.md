# Java Basics - Beginner's Guide

## 1. What is Java?
Java is a popular programming language used for building applications, websites, and games. It's known for "Write Once, Run Anywhere" - code works on any device with Java installed.

## 2. Setting Up Java
1. Download JDK (Java Development Kit) from Oracle or OpenJDK
2. Install it on your computer
3. Verify: Open terminal/command prompt and type `java -version`

## 3. Your First Java Program

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**How to run:**
1. Save as `HelloWorld.java`
2. Compile: `javac HelloWorld.java`
3. Run: `java HelloWorld`

## 4. Basic Syntax Rules
- Every Java program needs a **class**
- `main` method is the starting point
- Statements end with semicolon `;`
- Java is **case-sensitive**
- Use `//` for single-line comments, `/* */` for multi-line

## 5. Variables and Data Types

```java
public class Variables {
    public static void main(String[] args) {
        // Numbers
        int age = 25;                    // whole numbers
        double price = 99.99;            // decimal numbers
        
        // Text
        char grade = 'A';                // single character
        String name = "Hariharan";       // text/string
        
        // Boolean
        boolean isJavaFun = true;        // true or false
        
        // Print variables
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Price: " + price);
    }
}
```

## 6. Basic Operations

```java
public class Operations {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;
        
        System.out.println("Addition: " + (a + b));       // 15
        System.out.println("Subtraction: " + (a - b));    // 5
        System.out.println("Multiplication: " + (a * b)); // 50
        System.out.println("Division: " + (a / b));       // 2
        System.out.println("Remainder: " + (a % b));      // 0
    }
}
```

## 7. User Input

```java
import java.util.Scanner;

public class UserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        
        System.out.println("Hello " + name + ", you are " + age + " years old!");
        
        scanner.close();
    }
}
```

## 8. If-Else Statements

```java
public class IfElse {
    public static void main(String[] args) {
        int marks = 75;
        
        if (marks >= 90) {
            System.out.println("Grade: A");
        } else if (marks >= 75) {
            System.out.println("Grade: B");
        } else if (marks >= 60) {
            System.out.println("Grade: C");
        } else {
            System.out.println("Grade: F");
        }
    }
}
```

## 9. Loops

### For Loop
```java
public class ForLoop {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Number: " + i);
        }
    }
}
```

### While Loop
```java
public class WhileLoop {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println("Number: " + i);
            i++;
        }
    }
}
```

## 10. Practice Exercises

### Exercise 1: Simple Calculator
```java
public class Calculator {
    public static void main(String[] args) {
        int num1 = 20;
        int num2 = 10;
        
        System.out.println("Sum: " + (num1 + num2));
        System.out.println("Difference: " + (num1 - num2));
        System.out.println("Product: " + (num1 * num2));
        System.out.println("Quotient: " + (num1 / num2));
    }
}
```

### Exercise 2: Even or Odd
```java
public class EvenOdd {
    public static void main(String[] args) {
        int number = 7;
        
        if (number % 2 == 0) {
            System.out.println(number + " is even");
        } else {
            System.out.println(number + " is odd");
        }
    }
}
```

### Exercise 3: Print Multiplication Table
```java
public class MultiplicationTable {
    public static void main(String[] args) {
        int number = 5;
        
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + (number * i));
        }
    }
}
```

## Next Steps
1. Practice these examples by typing them yourself
2. Try modifying the code to see what happens
3. Complete the exercises
4. Experiment with different values
5. Learn about Arrays, Methods, and Object-Oriented Programming next

## Common Beginner Mistakes to Avoid
- Forgetting semicolons `;`
- Wrong class name (must match filename)
- Not closing braces `{}`
- Case sensitivity issues
- Forgetting to import Scanner for input

---
**Tips:**
- Practice daily, even 30 minutes helps
- Make mistakes - that's how you learn
- Use online compilers like repl.it or JDoodle if setup is difficult
- Join Java communities for help

Happy Coding! 🚀
