Java Full Course - Textbook Style (Extended Descriptions)

===================================

Lesson 1: Introduction + Hello World
-----------------------------------
Java is one of the most popular programming languages in the world. It is a high-level, object-oriented, and platform-independent language. Platform-independent means that Java programs can run on any device that has a Java Virtual Machine (JVM) installed. This feature makes it extremely versatile for software development across different operating systems.

Before writing Java programs, you need to install the Java Development Kit (JDK) which contains the Java compiler and runtime. After installation, you can check the version by opening a terminal or command prompt and typing `java -version`. This verifies that Java is installed correctly.

Your first Java program is the classic "Hello, World!" program. It demonstrates the structure of a Java program including classes, methods, and how output works.

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
- `public class Main` defines a class named Main.
- `public static void main(String[] args)` defines the main method where execution starts.
- `System.out.println()` prints text to the console.

To run:
1. Save the file as `Main.java`.
2. Compile with `javac Main.java`.
3. Run with `java Main`.


Lesson 2: Variables & Data Types
--------------------------------
Variables in Java act as containers to store data. Each variable has a name, type, and value. The type defines the kind of data it can hold, such as integers, decimals, or characters. Variables allow us to store information that can change over time.

Java is strongly typed, meaning you must declare the type of a variable before using it. Once a variable’s type is declared, it cannot store a different type of data.

Primitive data types in Java:
- `byte` (1 byte, small integers)
- `short` (2 bytes, medium integers)
- `int` (4 bytes, standard integers)
- `long` (8 bytes, very large integers)
- `float` (4 bytes, decimal numbers with less precision)
- `double` (8 bytes, decimal numbers with high precision)
- `char` (2 bytes, single character)
- `boolean` (1 bit, true or false)

Example:
```java
int age = 13;
double pi = 3.14159;
char grade = 'A';
boolean isSigma = true;
```
Constants can be declared with `final` keyword. Their values cannot be changed once assigned:
```java
final double PI = 3.14159;
```


Lesson 3: Operators
------------------
Operators perform operations on variables and values. Java has several types of operators:

1. Arithmetic Operators: +, -, *, /, % (for addition, subtraction, multiplication, division, and modulus)
2. Assignment Operators: =, +=, -=, *=, /=, %= (for assigning values and updating them)
3. Comparison Operators: ==, !=, >, <, >=, <= (for comparing values, results in true or false)
4. Logical Operators: &&, ||, ! (used with boolean values)
5. Increment/Decrement: ++, -- (increase or decrease by 1)

Example:
```java
int a = 10, b = 3;
System.out.println(a + b); // 13
```


Lesson 4: Strings
----------------
Strings are sequences of characters used to store text. Unlike primitive types, Strings are objects in Java and come with numerous built-in methods for manipulation and querying.

Operations include:
- Concatenation: joining two or more strings using `+`
- `.length()`: returns the number of characters
- `.charAt(index)`: returns the character at a specific position
- `.substring(start, end)`: extracts a part of a string
- `.toUpperCase()` / `.toLowerCase()`: changes case
- `.contains()`, `.startsWith()`, `.endsWith()`: check content
- `.equals()`: compare strings for content equality (not `==`)

Example:
```java
String name = "Avi";
System.out.println(name.length()); // 3
```


Lesson 5: Input & Output (Scanner)
---------------------------------
The Scanner class allows user input from the keyboard. It is part of `java.util` package, so it must be imported using `import java.util.Scanner;`. You can read text, integers, and decimals with `nextLine()`, `nextInt()`, and `nextDouble()`. Always close the Scanner after use.

Example:
```java
Scanner sc = new Scanner(System.in);
System.out.print("Enter name: ");
String name = sc.nextLine();
System.out.println("Hello, " + name);
sc.close();
```


Lesson 6: Conditional Statements
--------------------------------
Conditional statements allow decision-making in programs. Java supports `if`, `if-else`, `if-else if-else`, and `switch`.
- `if` checks a condition and executes code if true.
- `if-else` provides alternative code if false.
- `if-else if-else` handles multiple conditions.
- `switch` is used for multiple possible values of a variable.

Logical operators (`&&`, `||`, `!`) can be used to combine conditions.

Exercises:
1. Even or Odd
2. Voter Eligibility
3. Positive, Negative, or Zero
4. Grade Calculator
5. Simple Calculator with switch


Lesson 7: Loops
----------------
Loops are used to repeat code multiple times. Java supports `for`, `while`, and `do-while` loops.
- `for` loop: use when the number of iterations is known.
- `while` loop: use when the number of iterations is unknown; runs while condition is true.
- `do-while` loop: similar to while, but executes at least once.
- `break`: exit the loop immediately.
- `continue`: skip the current iteration.

Example:
```java
for(int i=1;i<=5;i++) System.out.println(i);
```


Lesson 8: Arrays
----------------
Arrays store multiple values of the same type in a single variable. Each element can be accessed by its index (starting from 0). Arrays can be declared with values or a fixed size. Looping through arrays is done with `for` or `for-each` loops.

Example:
```java
int[] numbers = {10,20,30};
for(int num: numbers) System.out.println(num);
```

Exercises for Arrays:
1. Input n numbers and calculate sum
2. Find largest and smallest number in an array
3. Input student marks and calculate average

===================================

All code examples are suitable for VS Code with JDK installed. Attempt exercises to reinforce concepts. Detailed understanding of variables, operators, strings, input/output, conditions, loops, and arrays forms the foundation of Java programming.

Java Intermediate Course - Chapters 9 to 16 - Full Descriptive Textbook Style

===================================

Chapter 9: Methods (Functions)
--------------------------------
Methods are **reusable blocks of code** designed to perform a specific task. They improve readability, reduce repetition, and help organize programs logically. Methods can take **input parameters** and return a **value**.

**Syntax:**
```java
modifier returnType methodName(parameters) {
    // method body
    return value; // if returnType is not void
}
```

**Example 1: Method without parameters**
```java
public static void greet() {
    System.out.println("Hello, Sigma Bro!");
}
```
**Example 2: Method with parameters**
```java
public static int add(int a, int b) {
    return a + b;
}
```
**Benefits of Methods:**
- Avoids code repetition
- Makes code organized and readable
- Easy debugging
- Can be reused in multiple programs

**Exercise:**
1. Create a method to calculate square of a number.
2. Create a method to check if a number is prime.

---

Chapter 10: Object-Oriented Programming (OOP Basics)
-----------------------------------------------------
OOP is programming using **objects** that represent real-world entities. Each object has **attributes (properties)** and **methods (behaviors)**. OOP helps in writing modular, reusable, and maintainable code.

**Key Concepts:**
1. **Class:** Blueprint/template for creating objects.
2. **Object:** Instance of a class.
3. **Encapsulation:** Hiding data and exposing only necessary access.
4. **Inheritance:** Reusing code from other classes.
5. **Polymorphism:** Objects can take many forms (method overloading/overriding).
6. **Abstraction:** Hiding complex details, showing essential features.

**Example: Creating a class and object**
```java
class Car {
    String color;
    String model;
    int year;
    void drive() {
        System.out.println(model + " is driving.");
    }
}
Car myCar = new Car();
myCar.color = "Red";
myCar.model = "Toyota";
myCar.drive();
```

**Constructors** initialize objects:
```java
Car car1 = new Car("Honda", 2022);
```

**Encapsulation example:**
```java
class Student {
    private String name;
    public void setName(String n) { name = n; }
    public String getName() { return name; }
}
```

---

Chapter 11: Inheritance & Polymorphism
--------------------------------------
**Inheritance** allows a class to inherit attributes and methods from another class, promoting code reuse.

**Example:**
```java
class Animal { void eat() { System.out.println("Animal eats"); } }
class Dog extends Animal { void bark() { System.out.println("Dog barks"); } }
```

**Polymorphism:**
- **Compile-time (Overloading):** Same method name, different parameters.
- **Runtime (Overriding):** Subclass changes parent method behavior.

**Exercise:**
1. Create a parent class `Shape` and child classes `Circle` and `Rectangle` with area methods.

---

Chapter 12: Encapsulation & Abstraction
--------------------------------------
**Encapsulation:** Protects data by using **private variables** and public getters/setters.
**Abstraction:** Shows only essential features using **abstract classes or interfaces**.

**Abstract Class Example:**
```java
abstract class Shape { abstract void area(); }
class Circle extends Shape { int radius; Circle(int r) { radius = r; } void area() { System.out.println(3.14*radius*radius); } }
```

**Exercise:**
1. Create an abstract class `Vehicle` and implement `Car` and `Bike` subclasses.

---

Chapter 13: Static & Instance Members
------------------------------------
- **Instance Members:** Belong to objects; each object has its own copy.
- **Static Members:** Belong to the class; shared across all objects.

**Example:**
```java
class Counter {
    static int count = 0;
    Counter() { count++; }
}
```
**Exercise:**
1. Create a `Student` class with static member tracking total students created.

---

Chapter 14: Constructors in Depth
--------------------------------
Constructors initialize objects. Types include:
- **Default constructor**: No parameters.
- **Parameterized constructor**: Takes arguments.
- **Copy constructor**: Create object from another object.

**Example:**
```java
class Student {
    String name;
    int age;
    Student(String n, int a) { name = n; age = a; }
}
```

**Exercise:**
1. Create a `Book` class with different constructors for title and author.

---

Chapter 15: Exception Handling
-----------------------------
Prevents program crashes by handling runtime errors.

**Keywords:** try, catch, finally, throw, throws.

**Example:**
```java
try {
    int result = 10 / 0;
} catch(ArithmeticException e) {
    System.out.println("Cannot divide by zero!");
} finally {
    System.out.println("End of program");
}
```

**Exercise:**
1. Handle input mismatch exception while reading integers from user.

---

Chapter 16: Packages & Import Statements
----------------------------------------
- **Package:** Group of related classes.
- **Import:** Allows use of classes from other packages.

**Example:**
```java
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
```

**Exercise:**
1. Create your own package `mypackage` with class `Utils` and import it in another class.

===================================

This intermediate textbook covers **Chapters 9 to 16** in full detail with examples, explanations, and exercises for practice.

Java Advanced Course - Chapters 17 to 24 - Full Descriptive Textbook Style

===================================

Chapter 17: Collections (ArrayList, HashMap, etc.)
--------------------------------------------------
Collections are used to **store and manage groups of objects** efficiently. Java provides various collection classes such as `ArrayList`, `HashMap`, `HashSet`, etc.

**ArrayList Example:**
```java
import java.util.ArrayList;
ArrayList<String> names = new ArrayList<>();
names.add("Avi");
names.add("Sigma");
System.out.println(names);
```

**HashMap Example:**
```java
import java.util.HashMap;
HashMap<String, Integer> marks = new HashMap<>();
marks.put("Avi", 90);
marks.put("Sigma", 95);
System.out.println(marks);
```

**Exercise:**
1. Create an ArrayList of integers and calculate the sum.
2. Create a HashMap to store student names and their grades.

---

Chapter 18: File Handling
------------------------
Java can **read from and write to files** using classes from `java.io` package.

**Example: Writing to a file**
```java
import java.io.FileWriter;
FileWriter fw = new FileWriter("file.txt");
fw.write("Hello World");
fw.close();
```

**Example: Reading from a file**
```java
import java.io.FileReader;
int ch;
FileReader fr = new FileReader("file.txt");
while((ch = fr.read()) != -1) {
    System.out.print((char)ch);
}
fr.close();
```

**Exercise:**
1. Create a file and write a list of names.
2. Read the file and count the number of lines.

---

Chapter 19: Recursion
---------------------
Recursion is a technique where a **method calls itself** to solve a problem. Base case is required to stop the recursion.

**Example: Factorial**
```java
int factorial(int n) {
    if(n <= 1) return 1;
    return n * factorial(n-1);
}
```

**Exercise:**
1. Write a recursive method to calculate Fibonacci numbers.
2. Write a recursive method to reverse a string.

---

Chapter 20: Interfaces & Abstract Classes
-----------------------------------------
- **Interface:** Only abstract methods, implemented by classes using `implements` keyword.
- **Abstract Class:** Can have both abstract and concrete methods, extended by subclasses.

**Interface Example:**
```java
interface Drawable {
    void draw();
}
class Circle implements Drawable {
    public void draw() {
        System.out.println("Drawing Circle");
    }
}
```

**Exercise:**
1. Create an interface `Vehicle` with methods `start` and `stop`.
2. Implement it in `Car` and `Bike` classes.

---

Chapter 21: Lambda Expressions & Streams
----------------------------------------
Lambda expressions provide a **concise way to represent anonymous methods**. Streams allow processing of collections efficiently.

**Example: Lambda with ArrayList**
```java
ArrayList<Integer> numbers = new ArrayList<>();
numbers.add(1);
numbers.add(2);
numbers.forEach(n -> System.out.println(n));
```

**Stream Example:**
```java
numbers.stream().filter(n -> n%2==0).forEach(System.out::println);
```

**Exercise:**
1. Filter all numbers greater than 10 using streams.
2. Print all strings starting with 'A' using lambda.

---

Chapter 22: Threads & Multithreading Basics
------------------------------------------
Multithreading allows **multiple tasks to run simultaneously**. Threads can be created by:
- Extending `Thread` class
- Implementing `Runnable` interface

**Example: Extending Thread**
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread running");
    }
}
MyThread t = new MyThread();
t.start();
```

**Exercise:**
1. Create two threads printing different messages simultaneously.

---

Chapter 23: GUI with Swing (Optional)
-------------------------------------
Swing provides components to build **Graphical User Interfaces**. Components include `JFrame`, `JButton`, `JLabel`, etc.

**Example:**
```java
import javax.swing.*;
public class Main {
    public static void main(String[] args) {
        JFrame frame = new JFrame("My GUI");
        JButton button = new JButton("Click Me");
        frame.add(button);
        frame.setSize(300,200);
        frame.setVisible(true);
    }
}
```

**Exercise:**
1. Create a simple calculator GUI.
2. Create a login form with username and password fields.

---

Chapter 24: Mini Projects / Practice
------------------------------------
Apply all knowledge from basic to advanced Java by building projects:
- **Calculator Program** (methods, loops)
- **Student Management System** (OOP, arrays, collections)
- **Banking System** (OOP, file handling, exception handling)
- **Simple Games** (loops, methods, OOP)
- **GUI Applications** (Swing, event handling)

**Exercise:**
1. Build a contact management program storing names and phone numbers using ArrayList.
2. Build a file-based library management system.

===================================

This textbook covers **Chapters 17 to 24** in detail with examples, explanations, and exercises for advanced Java topics.

Advanced Java Textbook: Beyond Chapter 24
===================================

Chapter 25: Java Memory Management & Garbage Collection
--------------------------------------------------------
Memory management is a core aspect of Java's runtime efficiency. Java handles memory automatically via the Garbage Collector (GC), which reclaims memory used by objects no longer referenced.

**Key Concepts:**
- **Heap Memory:** Stores all objects.
- **Stack Memory:** Stores local variables and function call information.
- **Garbage Collector (GC):** Runs automatically to free unused objects.

**GC Phases:**
1. **Marking:** Identifies reachable objects.
2. **Normal Deletion:** Removes unreferenced objects.
3. **Deletion with Compaction:** Frees memory and reduces fragmentation.

**Exercise:** Create a program that instantiates objects in a loop and observe GC with `System.gc()`.

---

Chapter 26: Java Reflection & Annotations
------------------------------------------
Reflection allows programs to inspect and modify runtime behavior, such as discovering class methods, fields, and constructors.

**Example:**
```java
Class<?> obj = Class.forName("java.lang.String");
Method[] methods = obj.getDeclaredMethods();
```
Annotations provide metadata for classes and methods, often used by frameworks for configuration.

**Exercise:** Define a custom annotation and process it using reflection.

---

Chapter 27: Java Native Interface (JNI)
---------------------------------------
JNI enables Java to call functions written in C/C++.
- **Use Cases:** Performance-critical operations, system-level calls.
- **Example:** Declare native methods in Java, implement them in C, and load libraries via `System.loadLibrary()`.

**Exercise:** Write a Java program that calls a C function using JNI.

---

Chapter 28: Java Virtual Machine (JVM) Internals
-------------------------------------------------
Understanding JVM internals is key to performance tuning.

**Components:**
- **Class Loader:** Loads classes into memory.
- **Bytecode Verifier:** Ensures code safety.
- **Execution Engine:** Executes bytecode.
- **Garbage Collector:** Handles memory cleanup.

**Exercise:** Monitor JVM using `jconsole` and identify memory usage patterns.

---

Chapter 29: Java Performance Tuning & Profiling
------------------------------------------------
Optimize applications by:
- Profiling code to identify bottlenecks (VisualVM, JProfiler).
- Tuning garbage collection parameters.
- Optimizing concurrency and thread management.

**Exercise:** Profile a multithreaded Java program and optimize memory usage.

---

Chapter 30: Java Security Best Practices
----------------------------------------
Secure Java applications by:
- Validating all user input.
- Encrypting sensitive data.
- Implementing authentication and authorization mechanisms.

**Exercise:** Encrypt and decrypt strings using Java's `Cipher` class.

---

Chapter 31: Java Design Patterns
--------------------------------
Common design patterns:
- **Singleton:** Single instance of a class.
- **Factory:** Object creation without specifying exact class.
- **Observer:** Objects subscribe to event notifications.

**Exercise:** Implement an Observer pattern for a stock market notification system.

---

Chapter 32: Java Microservices with Spring Boot
------------------------------------------------
Spring Boot simplifies microservices development:
- Embedded servers
- Auto-configuration
- Production-ready features (metrics, health checks)

**Exercise:** Build a RESTful API microservice with Spring Boot.

---

Chapter 33: Java Reactive Programming with Project Reactor
-----------------------------------------------------------
Reactive programming handles asynchronous data streams.
- **Flux:** 0..N items
- **Mono:** 0..1 item

**Exercise:** Process a stream of integers reactively and filter even numbers.

---

Chapter 34: Java Testing Frameworks & Best Practices
----------------------------------------------------
Use testing frameworks:
- **JUnit:** Unit testing
- **Mockito:** Mocking dependencies
- **TestNG:** Advanced testing scenarios

**Best Practices:**
- Write clear, readable tests.
- Test edge cases.
- Automate with CI/CD.

**Exercise:** Write JUnit tests for a banking application class.

===================================

This textbook covers advanced Java topics beyond Chapter 24 with detailed explanations, examples, and exercises, providing a comprehensive guide for professional Java development.

