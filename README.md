# JAVA Course for beginners
Java is a versatile, object-oriented programming language widely used for building enterprise-scale applications, mobile apps (Android), web applications, and more. Below, I’ll provide a sort of "all-in-one" Java guide with examples covering basic syntax, sorting algorithms, and Object-Oriented Programming (OOP) concepts.

# Table of Contents (JAVA)

1. [ Basic Java Syntax](#Basic-Java-Syntax)
2. [Variable](#Variable)
3. [Datatypes](#Datatypes)
4. [Operators](#Operators)
5. [if-else Statement](#if-else-Statement)
6. [Sorting Algorithms in Java](#Sorting-Algorithms-in-Java)
7. [Object-Oriented Programming (OOP) Concepts](#Object-Oriented-Programming-Concepts)
8. [Collections Framework](#Collections-Framework)
9. [File Handling](#File-Handling)
10. [Exception Handling](#Exception-Handling)
11. [ Multitnreading](#Multitnreading)

# Basic Java Syntax
### Hello World Program
```cs
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
# Variable

##  1: Integer Variable
```cs
public class IntegerVariable {
    public static void main(String[] args) {
        int age = 25; // Declaring and initializing an integer variable
        System.out.println("Age: " + age); // Output: Age: 25
    }
}
```
## 2: String Variable
```cs
public class StringVariable {
    public static void main(String[] args) {
        String name = "John Doe"; // Declaring and initializing a string variable
        System.out.println("Name: " + name); // Output: Name: John Doe
    }
}
```
## 3: Boolean Variable
```cs
public class BooleanVariable {
    public static void main(String[] args) {
        boolean isJavaFun = true; // Declaring and initializing a boolean variable
        System.out.println("Is Java fun? " + isJavaFun); // Output: Is Java fun? true
    }
}
```
## 4: Array Variable
```cs
public class ArrayVariable {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5}; // Declaring and initializing an array variable
        System.out.print("Numbers: ");
        for (int num : numbers) {
            System.out.print(num + " "); // Output: Numbers: 1 2 3 4 5
        }
    }
}
```
## 5: Double Variable
```cs
public class DoubleVariable {
    public static void main(String[] args) {
        double price = 19.99; // Declaring and initializing a double variable
        System.out.println("Price: " + price); // Output: Price: 19.99
    }
}
```
## 6: Character Variable
```cs
public class CharVariable {
    public static void main(String[] args) {
        char grade = 'A'; // Declaring and initializing a character variable
        System.out.println("Grade: " + grade); // Output: Grade: A
    }
}
```
## 7: Float Variable
```cs
public class FloatVariable {
    public static void main(String[] args) {
        float pi = 3.14f; // Declaring and initializing a float variable
        System.out.println("Pi: " + pi); // Output: Pi: 3.14
    }
}
```
## 8: Long Variable
```cs
public class LongVariable {
    public static void main(String[] args) {
        long distance = 100000000L; // Declaring and initializing a long variable
        System.out.println("Distance: " + distance); // Output: Distance: 100000000
    }
}

```



# Datatypes 
### A. Primitive -  B. Non-Primitive
## (A) Primitive Data Types 
### 1. byte || Size: 8 bits || Range: -128 to 127

Example:

```cs
byte b = 100;
System.out.println("byte: " + b);
```
### 2. short || Size: 16 bits || Range: -32,768 to 32,767

Example:

```cs
short s = 10000;
System.out.println("short: " + s);
```
### 3. int || Size: 32 bits || Range: -2^31 to 2^31-1

Example:

```cs
int i = 100000;
System.out.println("int: " + i);
```
### 4. long || Size: 64 bits || Range: -2^63 to 2^63-1

Example:

```cs
long l = 100000L;
System.out.println("long: " + l);
```
### 5. float || Size: 32 bits || Single-precision floating point

Example:

```cs
float f = 5.75f;
System.out.println("float: " + f);
```
### 6. double || Size: 64 bits || Double-precision floating point

Example:

```cs
double d = 19.99;
System.out.println("double: " + d);
```
### 7. boolean || Size: Varies (depends on JVM implementation) || Values: true or false

Example:

```cs
boolean isJavaFun = true;
System.out.println("boolean: " + isJavaFun);
```
### 8. char

Size: 16 bits

Single Unicode character

Example:

```cs
char letter = 'A';
System.out.println("char: " + letter);
```
## (B) Non-Primitive Data Types
### 1. String

A sequence of characters

Example:

```
String greeting = "Hello, World!";
System.out.println("String: " + greeting);
```
### 2. Array

A collection of elements of the same type

Example:

```cs
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println("Array element: " + num);
}
```







# Operators
### 1. Arithmetic Operators:
Used to perform basic arithmetic operations.

```cs
int a = 10;
int b = 5;
System.out.println("Addition: " + (a + b)); // 15
System.out.println("Subtraction: " + (a - b)); // 5
System.out.println("Multiplication: " + (a * b)); // 50
System.out.println("Division: " + (a / b)); // 2
System.out.println("Modulus: " + (a % b)); // 0
```
### 2. Relational Operators:
Used to compare two values.

```cs
int a = 10;
int b = 5;
System.out.println("Equal: " + (a == b)); // false
System.out.println("Not Equal: " + (a != b)); // true
System.out.println("Greater Than: " + (a > b)); // true
System.out.println("Less Than: " + (a < b)); // false
System.out.println("Greater Than or Equal To: " + (a >= b)); // true
System.out.println("Less Than or Equal To: " + (a <= b)); // false
```
### 3. Logical Operators: 
Used to perform logical operations.

```cs
boolean x = true;
boolean y = false;
System.out.println("AND: " + (x && y)); // false
System.out.println("OR: " + (x || y)); // true
System.out.println("NOT: " + (!x)); // false
```
### 4. Assignment Operators: 
Used to assign values to variables.

```cs
int a = 10;
a += 5; // a = a + 5
System.out.println("a += 5: " + a); // 15
a -= 3; // a = a - 3
System.out.println("a -= 3: " + a); // 12
a *= 2; // a = a * 2
System.out.println("a *= 2: " + a); // 24
a /= 4; // a = a / 4
System.out.println("a /= 4: " + a); // 6
a %= 2; // a = a % 2
System.out.println("a %= 2: " + a); // 0
```
### 5. Increment and Decrement Operators: 
Used to increment or decrement the value of a variable.

```cs
int a = 10;
System.out.println("Original Value: " + a); // 10
System.out.println("Post Increment: " + (a++)); // 10
System.out.println("After Post Increment: " + a); // 11
System.out.println("Pre Increment: " + (++a)); // 12
System.out.println("Post Decrement: " + (a--)); // 12
System.out.println("After Post Decrement: " + a); // 11
System.out.println("Pre Decrement: " + (--a)); // 10
```
### 6. Ternary Operator
The ternary operator in Java is a shorthand for the if-else statement. It is also known as the conditional operator. It allows you to make decisions in a compact way. 
```cs
condition ? expression1 : expression2
```
If the condition is true, expression1 is executed. If the condition is false, expression2 is executed.

Example
Here is an example to illustrate the use of the ternary operator:

```cs
public class TernaryOperatorExample {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;
        
        // Using the ternary operator
        int max = (a > b) ? a : b;
        
        System.out.println("The maximum value is: " + max);
    }
}
```

### 7.1 Increment Operator (++)
The increment operator adds one to the value of a variable.

```cs
public class Main {
    public static void main(String[] args) {
        int a = 5;
        a++; // Post-increment: a is now 6
        System.out.println(a); // Output: 6

        int b = 5;
        ++b; // Pre-increment: b is now 6
        System.out.println(b); // Output: 6
    }
}
```
### 7.2 Decrement Operator (--)
The decrement operator subtracts one from the value of a variable.

```cs
public class Main {
    public static void main(String[] args) {
        int x = 5;
        x--; // Post-decrement: x is now 4
        System.out.println(x); // Output: 4

        int y = 5;
        --y; // Pre-decrement: y is now 4
        System.out.println(y); // Output: 4
    }
}
```
Post-Increment/Decrement (a++, x--): The value is used in the expression first, and then incremented or decremented.

Pre-Increment/Decrement (++b, --y): The value is incremented or decremented first, and then used in the expression.


## if-else Statement
The if-else statement allows you to execute a block of code based on a condition.

```cs
int age = 18;

if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are not an adult.");
}
```
The if-else if-else ladder allows you to test multiple conditions.

```cs
int score = 75;

if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B");
} else if (score >= 70) {
    System.out.println("Grade: C");
} else if (score >= 60) {
    System.out.println("Grade: D");
} else {
    System.out.println("Grade: F");
}
```
## switch Statement
The switch statement allows you to execute a block of code based on the value of a variable.

```cs
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
        break;
}

```




# Sorting Algorithms in Java
### Bubble Sort
```cs
public class BubbleSort {
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    // Swap arr[j] and arr[j+1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }

    public static void main(String[] args) {
        int[] arr = {64, 34, 25, 12, 22, 11, 90};
        bubbleSort(arr);
        System.out.println("Sorted array:");
        for (int i : arr) {
            System.out.print(i + " ");
        }
    }
}
```
### Quick Sort
```cs
public class QuickSort {
    public static void quickSort(int[] arr, int low, int high) {
        if (low < high) {
            int pi = partition(arr, low, high);
            quickSort(arr, low, pi - 1);
            quickSort(arr, pi + 1, high);
        }
    }

    private static int partition(int[] arr, int low, int high) {
        int pivot = arr[high];
        int i = low - 1;
        for (int j = low; j < high; j++) {
            if (arr[j] < pivot) {
                i++;
                // Swap arr[i] and arr[j]
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
        // Swap arr[i+1] and arr[high] (pivot)
        int temp = arr[i + 1];
        arr[i + 1] = arr[high];
        arr[high] = temp;
        return i + 1;
    }

    public static void main(String[] args) {
        int[] arr = {10, 7, 8, 9, 1, 5};
        quickSort(arr, 0, arr.length - 1);
        System.out.println("Sorted array:");
        for (int i : arr) {
            System.out.print(i + " ");
        }
    }
}
```
# Object-Oriented Programming Concepts
## Classes and Objects
```cs
class Dog {
    // Fields (attributes)
    String name;
    int age;

    // Constructor
    public Dog(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method
    public void bark() {
        System.out.println(name + " says: Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog("Buddy", 3);
        myDog.bark(); // Output: Buddy says: Woof!
    }
}
```
## Inheritance
Inheritance in Java is a mechanism that allows one class (the child or subclass) to inherit the fields and methods of another class (the parent or superclass). This helps in code reusability and the creation of a hierarchical classification. Inheritance represents the "is-a" relationship, meaning a subclass is a type of the superclass.
```cs
public class Demo {
    // The main class where the program execution begins
    public static void main(String[] args) {
        // Creating an instance of the Cat class and assigning it to the Animal reference 'om'
        Animal om = new Cat();
        // Creating an instance of the Dog class and assigning it to the Animal reference 'om1'
        Animal om1 = new Dog();
        // Calling the overridden New method of the Cat class
        om.New();
        // Calling the overridden New method of the Dog class
        om1.New();
    }
}

class Animal {
    int age; // Instance variable to store the age of the animal
    String name; // Instance variable to store the name of the animal

    void New() {
        // Method to print the age and name of the animal (this method will be overridden in subclasses)
        System.out.println(age + name);
    }
}

class Dog extends Animal {
    @Override
    void New() {
        // Overriding the New method of the Animal class
        age = 20; // Setting the age of the dog
        name = "Mukherjee"; // Setting the name of the dog
        // Printing the age and name of the dog
        System.out.println(age + name);
    }
}

class Cat extends Animal {
    @Override
    void New() {
        // Overriding the New method of the Animal class
        age = 22; // Setting the age of the cat
        name = "Soumik"; // Setting the name of the cat
        int id = 202; // Local variable to store the id of the cat
        // Printing the age, name, and id of the cat
        System.out.println(age + name + id);
    }
}

```
### 1. Single Inheritance
A single class inherits from one superclass.

```cs
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
        dog.bark();
    }
}
```
### 2. Multilevel Inheritance
A class is derived from another class, which is also derived from another class.

```cs
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Mammal extends Animal {
    void walk() {
        System.out.println("Walking...");
    }
}

class Dog extends Mammal {
    void bark() {
        System.out.println("Barking...");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
        dog.walk();
        dog.bark();
    }
}
```
### 3. Hierarchical Inheritance
Multiple classes inherit from one superclass.

```cs
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("Meowing...");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
        dog.bark();

        Cat cat = new Cat();
        cat.eat();
        cat.meow();
    }
}
```
### 4. Hybrid Inheritance (Using Interfaces)
A combination of two or more types of inheritance. Java supports it through interfaces.

```cs
interface Animal {
    void eat();
}

class Mammal implements Animal {
    public void eat() {
        System.out.println("Eating...");
    }
}

interface Pet {
    void play();
}

class Dog extends Mammal implements Pet {
    public void play() {
        System.out.println("Playing...");
    }

    void bark() {
        System.out.println("Barking...");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
        dog.play();
        dog.bark();
    }
}
```
## Polymorphism (Method Overriding)
## 1. Compile-time Polymorphism ( Method Overloading )
This happens when multiple methods in the same class have the same name but different parameters. It is a way to achieve compile-time polymorphism.

```cs
class Adder {
    static int add(int a, int b) {
        return a + b;
    }

    static double add(double a, double b) {
        return a + b;
    }
}

public class TestOverloading {
    public static void main(String[] args) {
        System.out.println(Adder.add(10, 20));      // Output: 30
        System.out.println(Adder.add(10.5, 20.5));  // Output: 31.0
    }
}
```
## 2. Runtime Polymorphism ( Method Overriding )
This occurs when a subclass provides a specific implementation for a method that is already defined in its superclass. It's a way to achieve runtime polymorphism.

```cs
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class TestPolymorphism {
    public static void main(String[] args) {
        Animal myAnimal = new Dog();
        myAnimal.sound();  // Output: Dog barks
    }
}

```
## Encapsulation
```cs
class Person {
    private String name; // Private field

    // Getter
    public String getName() {
        return name;
    }

    // Setter
    public void setName(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("John");
        System.out.println("Name: " + person.getName()); // Output: Name: John
    }
}
```
## Abstraction (Using Abstract Class)
```cs
abstract class Shape {
    abstract void draw(); // Abstract method
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a Circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape myShape = new Circle();
        myShape.draw(); // Output: Drawing a Circle
    }
}
```
## interfaces :
```cs
// Define an interface named Animal
interface Animal {
    // This variable is implicitly public, static, and final
    int LEGS = 4;

    // This method is implicitly public and abstract
    void sound();
}

// Define an interface named Pet
interface Pet {
    // This method is implicitly public and abstract
    void play();
}

// Implement both interfaces in a class named Dog
class Dog implements Animal, Pet {
    // Provide the implementation for the sound method
    public void sound() {
        System.out.println("Woof");
        System.out.println("Dogs have " + LEGS + " legs.");
    }

    // Provide the implementation for the play method
    public void play() {
        System.out.println("The dog is playing.");
    }
}

// Implement both interfaces in a class named Cat
class Cat implements Animal, Pet {
    // Provide the implementation for the sound method
    public void sound() {
        System.out.println("Meow");
        System.out.println("Cats have " + LEGS + " legs.");
    }

    // Provide the implementation for the play method
    public void play() {
        System.out.println("The cat is playing.");
    }
}

// Class to test the implementation
public class InterfaceExample {
    public static void main(String[] args) {
        // Create an instance of Dog
        Dog myDog = new Dog();
        // Create an instance of Cat
        Cat myCat = new Cat();
        
        // Call the sound and play methods on Dog instance
        myDog.sound();
        myDog.play();

        // Call the sound and play methods on Cat instance
        myCat.sound();
        myCat.play();
    }
}

```
#  Collections Framework
## 1. List
Lists allow duplicate elements and maintain the order of insertion.

Example using ArrayList:

```cs
import java.util.ArrayList;

public class ListExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Apple");

        for (String item : list) {
            System.out.println(item);
        }
    }
}
```
## 2. Set
Sets do not allow duplicate elements and do not guarantee any order.

Example using HashSet:

```cs
import java.util.HashSet;

public class SetExample {
    public static void main(String[] args) {
        HashSet<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Apple");

        for (String item : set) {
            System.out.println(item);
        }
    }
}
```
## 3. Map
Maps store key-value pairs. Keys must be unique, but values can be duplicated.

Example using HashMap:

```cs
import java.util.HashMap;

public class MapExample {
    public static void main(String[] args) {
        HashMap<Integer, String> map = new HashMap<>();
        map.put(1, "Apple");
        map.put(2, "Banana");
        map.put(1, "Cherry");

        for (Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }
    }
}
```
## Summary of Key Differences
#### List: Allows duplicates || Maintains insertion order

#### Set: Does not allow duplicates || No guaranteed order (unless using LinkedHashSet or TreeSet)

#### Map: Stores key-value pairs || Keys must be unique

# File Handling
## Reading a File
```cs
import java.io.File;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");
            Scanner reader = new Scanner(file);
            while (reader.hasNextLine()) {
                String data = reader.nextLine();
                System.out.println(data);
            }
            reader.close();
        } catch (Exception e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }
}
```
# Exception Handling
## Types of Exceptions:

### 1. Checked Exceptions: 
These are exceptions that are checked at compile-time. For example, IOException and SQLException.

### 2. Unchecked Exceptions: 
These are exceptions that are checked at runtime. For example, NullPointerException and ArithmeticException.

### 3. Errors: 
These are serious problems that a reasonable application should not try to catch. For example, OutOfMemoryError and StackOverflowError.

## Key Components:

### 1. try block: 
The code that might throw an exception is placed inside the try block.

### 2. catch block: 
This block catches and handles the exception.

### 3. finally block: 
This block executes regardless of whether an exception occurred or not. It's typically used for resource cleanup.

### 4. throw keyword: 
Used to explicitly throw an exception.

### 5. throws keyword: 
Used in method signatures to declare the exceptions that a method can throw.
## 1. try Block
The try block contains the code that might throw an exception. Only the code that might throw an exception should be placed inside the try block.

```cs
try {
    // Code that may throw an exception
} catch (ExceptionType e) {
    // Code to handle the exception
}
```
## 2. catch Block
The catch block handles the exception that occurs in the try block. It can have multiple catch clauses to handle different types of exceptions.

```cs
try {
    int[] numbers = {1, 2, 3};
    System.out.println(numbers[5]); // This will throw an ArrayIndexOutOfBoundsException
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Array index is out of bounds!");
} catch (Exception e) {
    System.out.println("An exception occurred!");
}
```
## 3. finally Block
The finally block contains code that is executed regardless of whether an exception occurred or not. It’s commonly used for cleanup activities, like closing a file or releasing resources.

```cs
try {
    int[] numbers = {1, 2, 3};
    System.out.println(numbers[5]);
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Array index is out of bounds!");
} finally {
    System.out.println("This block is always executed.");
}
```
### 4. throw Keyword
The throw keyword is used to explicitly throw an exception. It is usually used when you want to indicate that something unexpected has happened.

```cs
public void checkAge(int age) {
    if (age < 18) {
        throw new IllegalArgumentException("Age must be 18 or older.");
    }
}
```
### 5. throws Keyword
The throws keyword is used in method signatures to declare the exceptions that a method can throw. This informs the caller of the method that it needs to handle these exceptions.

```cs
public void readFile() throws IOException {
    FileInputStream fis = new FileInputStream("file.txt");
    int data;
    while ((data = fis.read()) != -1) {
        System.out.print((char) data);
    }
}
```
Comprehensive Example
Here’s a complete example that includes all the components:
```cs
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;

public class ExceptionHandlingExample {

    public static void main(String[] args) {
        try {
            readFile("file.txt");
        } catch (IOException e) {
            System.out.println("An IOException occurred: " + e.getMessage());
        }
    }

    public static void readFile(String fileName) throws IOException {
        FileInputStream fis = null;
        try {
            fis = new FileInputStream(fileName);
            int data;
            while ((data = fis.read()) != -1) {
                System.out.print((char) data);
            }
        } catch (FileNotFoundException e) {
            System.out.println("File not found: " + fileName);
        } finally {
            if (fis != null) {
                try {
                    fis.close();
                } catch (IOException e) {
                    System.out.println("Error closing the file.");
                }
            }
        }
    }
}
```
Explanation:

try block: Contains code that attempts to open and read a file.

catch block: Handles FileNotFoundException if the file is not found.

finally block: Ensures that the FileInputStream is closed, regardless of whether an exception occurred.
## Custom exception class
```cs
// Custom exception class
class SoumikException extends Exception {
    // Constructor that accepts a custom error message
    public SoumikException(String message) {
        super(message);
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        try {
            checkCondition(false);
        } catch (SoumikException e) {
            System.out.println("Caught SoumikException: " + e.getMessage());
        }
    }

    // Method that throws SoumikException
    public static void checkCondition(boolean condition) throws SoumikException {
        if (!condition) {
            throw new SoumikException("Condition failed!");
        }
    }
}
```


# Multitnreading

Multithreading in Java is a powerful feature that allows you to perform multiple tasks concurrently within a single program. This can significantly improve the performance of your application by making better use of CPU resources. Java provides built-in support for multithreading through the java.lang.Thread class and the java.util.concurrent package.

Here's a basic example to demonstrate multithreading in Java:

```cs
class MyThread extends Thread {
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println(Thread.currentThread().getId() + " Value " + i);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
        t1.start();
        t2.start();
    }
}
```
OutPut
```cs
12 Value 0
11 Value 0
12 Value 1
11 Value 1
12 Value 2
11 Value 2
12 Value 3
11 Value 3
12 Value 4
11 Value 4
```
In this example, we define a class MyThread that extends the Thread class and overrides the run method. The main method creates two instances of MyThread and starts them, resulting in two threads running concurrently.

## 1. What is a Thread in Java?
Explanation: A thread is a lightweight process and the smallest unit of execution within a program. Java provides built-in support for multithreading, enabling concurrent execution of two or more parts of a program for maximum utilization of CPU.

Example:

```cs
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running.");
    }

    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();
    }
}
```
## life cycle of a thread
The life cycle of a thread in Java includes several stages, often referred to as states. Here's a concise summary of each state:

 New: The thread is created but not yet started. It's in the "new" state.

 Runnable: After calling the start() method, the thread moves to the "runnable" state. It is ready to run but may be waiting for CPU resources.

 Blocked/Waiting: The thread might move to this state if it's waiting for a monitor lock or another thread to complete its task. There are specific states within this category:

Blocked: Waiting to acquire a lock.

Waiting: Waiting indefinitely for another thread to perform a particular action.

Timed Waiting: Waiting for another thread to perform an action for a specified period.

Timed Waiting: Similar to "waiting," but the thread remains in this state for a specified amount of time before automatically transitioning.

Terminated: Once the thread's run() method completes, it transitions to the "terminated" state, indicating that the thread's execution has finished.

Here's a simple code example demonstrating a basic thread in Java:

```cs
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running...");
    }

    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();  // Moves the thread to the runnable state
    }
}
```
## 2. What is the difference between Thread and Runnable?
Explanation: The Thread class provides the ability to create a thread by extending it, while the Runnable interface is used to implement threads by passing an instance of a class that implements Runnable to a Thread object.

Example:

```cs
// Using Thread class
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running.");
    }
}

// Using Runnable interface
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Thread is running.");
    }
}

public class Test {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();

        Thread t2 = new Thread(new MyRunnable());
        t2.start();
    }
}
```
## 3. What is synchronization in Java?
Explanation: Synchronization is the process of controlling the access of multiple threads to shared resources. It prevents thread interference and memory consistency errors.

Example:

```cs
class Counter {
    private int count = 0;

    // Synchronized method
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class Test {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println("Count: " + counter.getCount());
    }
}
```
## 4. What is a deadlock and how can it be avoided?
Explanation: A deadlock is a situation where two or more threads are blocked forever, waiting for each other. Deadlock can be avoided by careful design of resource allocation and avoiding circular dependencies.

Example:

```cs
class A {
    synchronized void methodA(B b) {
        System.out.println("Thread 1 starts execution of methodA()");
        try { Thread.sleep(100); } catch (InterruptedException e) {}

        System.out.println("Thread 1 trying to call B's methodB()");
        b.methodB();
    }

    synchronized void methodB() {
        System.out.println("Inside methodA() of A");
    }
}

class B {
    synchronized void methodA(A a) {
        System.out.println("Thread 2 starts execution of methodA()");
        try { Thread.sleep(100); } catch (InterruptedException e) {}

        System.out.println("Thread 2 trying to call A's methodB()");
        a.methodB();
    }

    synchronized void methodB() {
        System.out.println("Inside methodB() of B");
    }
}

public class Test {
    public static void main(String[] args) {
        final A a = new A();
        final B b = new B();

        Thread t1 = new Thread(() -> a.methodA(b));
        Thread t2 = new Thread(() -> b.methodA(a));

        t1.start();
        t2.start();
    }
}
```
## 5. What is Thread Pool and how to create one in Java?
Explanation: A Thread Pool is a pool of worker threads that are managed and maintained by a framework or service. Using a thread pool can improve the performance of a program by reducing the overhead of creating and destroying threads.

Example:

```cs
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class Test {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(5);

        for (int i = 0; i < 10; i++) {
            Runnable worker = new WorkerThread("" + i);
            executor.execute(worker);
        }

        executor.shutdown();
        while (!executor.isTerminated()) {}

        System.out.println("Finished all threads");
    }
}

class WorkerThread implements Runnable {
    private String command;

    public WorkerThread(String s) {
        this.command = s;
    }

    @Override
    public void run() {
        System.out.println(Thread.currentThread().getName() + " Start. Command = " + command);
        processCommand();
        System.out.println(Thread.currentThread().getName() + " End.");
    }

    private void processCommand() {
        try { Thread.sleep(5000); } catch (InterruptedException e) { e.printStackTrace(); }
    }

    @Override
    public String toString() {
        return this.command;
    }
}
```

✅ 1. Java Fundamentals
1.	What is Java?
2.	What are the features of Java?
3.	Explain JVM, JRE, and JDK.
4.	What is the difference between JDK and JRE?
5.	What is bytecode in Java?
6.	Why is Java platform-independent?
7.	What are the different types of memory areas allocated by JVM?
8.	Explain the Java program execution process.
9.	What is the main() method in Java?
10.	Why is Java not 100% object-oriented?
________________________________________
✅ 2. Data Types and Variables
11.	What are the different data types in Java?
12.	What is the difference between primitive and non-primitive data types?
13.	What is type casting? Explain implicit and explicit casting.
14.	What is a variable in Java?
15.	What are static variables and instance variables?
16.	What are final variables?
________________________________________
✅ 3. Operators
17.	What are the types of operators in Java?
18.	What is the difference between == and .equals()?
19.	What is the difference between && and &?
20.	What is the instanceof operator?
________________________________________
✅ 4. Control Statements
21.	What are control flow statements in Java?
22.	Difference between if and switch statement?
23.	What are loop control structures in Java?
24.	What is the difference between break and continue?
________________________________________
✅ 5. Arrays and Strings
25.	How are arrays declared and initialized in Java?
26.	What are the types of arrays in Java?
27.	What is the difference between Array and ArrayList?
28.	What is a String in Java?
29.	Difference between String, StringBuffer, and StringBuilder?
30.	Why are Strings immutable in Java?
31.	How does String intern pool work?
________________________________________
✅ 6. Methods and Constructors
32.	What is a method in Java?
33.	What is method overloading?
34.	What is a constructor?
35.	Difference between constructor and method?
36.	What is constructor overloading?
37.	What is the use of the ‘this’ keyword?
________________________________________
✅ 7. Object-Oriented Programming (OOP)
38.	What are the four pillars of OOP?
39.	Explain the concept of inheritance.
40.	What is method overriding?
41.	What is the use of the ‘super’ keyword?
42.	Difference between overloading and overriding.
43.	What is abstraction?
44.	What is an abstract class?
45.	What is an interface?
46.	What is polymorphism?
47.	What is encapsulation?
48.	Can an interface extend another interface?
49.	Can a class implement multiple interfaces?
50.	Difference between interface and abstract class?
________________________________________
✅ 8. Access Modifiers
51.	What are access modifiers in Java?
52.	Explain public, private, protected, and default.
53.	What is the use of private constructors?
________________________________________
✅ 9. Packages and Imports
54.	What is a package in Java?
55.	How do you create and import packages?
56.	Difference between import java.* and import java.util.*?
________________________________________
✅ 10. Exception Handling
57.	What is exception handling in Java?
58.	What is the difference between checked and unchecked exceptions?
59.	What are try, catch, finally, throw, and throws?
60.	What is the difference between throw and throws?
61.	What is a custom exception?
________________________________________
✅ 11. Wrapper Classes and Autoboxing
62.	What are wrapper classes?
63.	What is autoboxing and unboxing?
64.	Why do we need wrapper classes?
________________________________________
✅ 12. Static and Final Keywords
65.	What is a static method?
66.	Can we override static methods?
67.	What is a final class?
68.	Can a final method be overridden?
69.	What is the difference between final, finally, and finalize()?
________________________________________
✅ 13. Inner Classes
70.	What are inner classes in Java?
71.	What is a static nested class?
72.	What is a local inner class?
73.	What is an anonymous inner class?
________________________________________
✅ 14. Miscellaneous
74.	What is the default value of local variables?
75.	What is the difference between == and equals()?
76.	What is the difference between heap and stack memory?
77.	What is garbage collection in Java?
78.	How does garbage collector work?
79.	What are transient and volatile keywords?
80.	Can we override the main method?
81.	What is System.out.println()?
82.	What is the difference between public static void main and static public void main?
83.	Can we declare a class as static?
84.	What is the default constructor?
________________________________________
✅ 1. Basic OOP Principles
1.	What is Object-Oriented Programming?
2.	What are the four main principles of OOP?
3.	What is an object in Java?
4.	What is a class in Java?
5.	Difference between a class and an object?
6.	What is the purpose of OOP?
________________________________________
✅ 2. Encapsulation
7.	What is encapsulation?
8.	How is encapsulation implemented in Java?
9.	What are the advantages of encapsulation?
10.	Can you give a real-world example of encapsulation?
________________________________________
✅ 3. Abstraction
11.	What is abstraction?
12.	How do you achieve abstraction in Java?
13.	Difference between abstract class and interface?
14.	What is an abstract method?
15.	Can we create an object of an abstract class?
16.	Can abstract classes have constructors?
17.	Can abstract classes have non-abstract methods?
18.	Why do we need abstraction?
19.	Give real-life examples of abstraction in Java.
________________________________________
✅ 4. Inheritance
20.	What is inheritance in Java?
21.	What are the types of inheritance supported in Java?
22.	Why doesn’t Java support multiple inheritance with classes?
23.	What is the ‘super’ keyword in Java?
24.	How do you call the parent class constructor?
25.	Can constructors be inherited?
26.	What is the difference between IS-A and HAS-A relationships?
27.	What is hierarchical inheritance?
28.	What are the benefits of inheritance?
________________________________________
✅ 5. Polymorphism
29.	What is polymorphism?
30.	What is method overloading?
31.	What is method overriding?
32.	Difference between compile-time and runtime polymorphism?
33.	Can we override static methods?
34.	Can we override private methods?
35.	What is covariant return type?
36.	What is dynamic method dispatch?
37.	What is the role of polymorphism in OOP design?
________________________________________
✅ 6. Interface and Abstract Class
38.	What is an interface in Java?
39.	What is the difference between interface and abstract class?
40.	Can an interface extend another interface?
41.	Can a class implement multiple interfaces?
42.	What happens if two interfaces have the same method signature?
43.	What is a marker interface?
44.	What is functional interface (Java 8)?
45.	Can an interface have static methods?
46.	Can an interface have private methods (Java 9+)?
________________________________________
✅ 7. Class Members & Access Control
47.	What is the difference between static and instance methods?
48.	What is the use of ‘this’ keyword?
49.	What is the use of ‘super’ keyword?
50.	What is method hiding in Java?
51.	Can we override a final method?
52.	What are access modifiers and how do they relate to OOP?
53.	Difference between public, private, protected, and default access modifiers?
________________________________________
✅ 8. Constructors
54.	What is a constructor?
55.	What is constructor overloading?
56.	Can constructors be overridden?
57.	Can an abstract class have a constructor?
58.	What is a copy constructor in Java?
________________________________________
✅ 9. Object Class and Overriding Methods
59.	What is the Object class in Java?
60.	Which methods are defined in Object class?
61.	Why should you override toString(), equals(), and hashCode() methods?
62.	What is the contract between equals() and hashCode()?
63.	What is the difference between == and .equals()?
________________________________________
✅ 10. Final, Static, and Other Keywords
64.	What is a final class?
65.	Can we inherit a final class?
66.	What is the difference between final, finally, and finalize()?
67.	Can we override a static method?
68.	What is static binding and dynamic binding?
________________________________________
✅ 11. Design and Relationships
69.	What is association in OOP?
70.	What is aggregation vs composition?
71.	What is dependency in OOP?
72.	What are coupling and cohesion?
73.	What is object cloning? How is it achieved in Java?
74.	What is deep copy vs shallow copy?
________________________________________
✅ 12. Advanced OOP Design Topics
75.	What is the SOLID principle?
76.	What is the Liskov Substitution Principle?
77.	What is the Open/Closed Principle?
78.	How do interfaces promote loose coupling?
79.	What is the importance of design patterns in OOP?
80.	What is a singleton class?
81.	How is immutability implemented in Java?
82.	How does Java handle memory for objects?
________________________________________
✅ 1. Basics of Multithreading
1.	What is multithreading in Java?
2.	What is the difference between process and thread?
3.	What are the advantages of multithreading?
4.	What is the lifecycle of a thread?
5.	What is the difference between multitasking and multithreading?
6.	What is the difference between user thread and daemon thread?
7.	How do you create a thread in Java?
8.	Difference between extending Thread and implementing Runnable?
9.	Can we start a thread twice?
10.	What happens if we call run() method directly instead of start()?
________________________________________
✅ 2. Thread Lifecycle & Methods
11.	What are the different states of a thread?
12.	What does the start() method do?
13.	What is the use of yield() method?
14.	What is the sleep() method? Can a thread sleep forever?
15.	What is the join() method? How is it used?
16.	What happens if one thread calls join() on another?
17.	What is the difference between sleep() and wait()?
18.	What is the difference between notify() and notifyAll()?
19.	What is thread priority?
20.	What is the default priority of a thread?
21.	Can thread priority guarantee execution order?
________________________________________
✅ 3. Synchronization
22.	What is synchronization in Java?
23.	What is a critical section?
24.	How do you achieve synchronization in Java?
25.	What is the synchronized keyword?
26.	What is the difference between synchronized method and synchronized block?
27.	Can we synchronize a static method?
28.	What is object-level lock and class-level lock?
29.	What is the drawback of synchronization?
30.	How does Java avoid race conditions?
________________________________________
✅ 4. Concurrency Issues
31.	What is a race condition?
32.	What is thread interference?
33.	What is deadlock?
34.	How to prevent deadlock in Java?
35.	What is livelock?
36.	What is starvation?
37.	What is thread-safe code?
38.	What is reentrant synchronization?
________________________________________
✅ 5. Daemon Threads
39.	What is a daemon thread?
40.	How do you create a daemon thread?
41.	What is the difference between daemon thread and user thread?
42.	Can you make the main thread a daemon thread?
________________________________________
✅ 6. Inter-thread Communication
43.	What is inter-thread communication?
44.	What are the methods used for inter-thread communication?
45.	Why wait(), notify(), and notifyAll() must be called in synchronized blocks?
46.	What is the purpose of wait() method?
47.	Can we call wait() outside synchronized block?
________________________________________
✅ 7. Java Memory Model & Volatile
48.	What is the Java Memory Model (JMM)?
49.	What is the use of the volatile keyword?
50.	How is volatile different from synchronized?
51.	Is volatile enough to make a class thread-safe?
________________________________________
✅ 8. Thread Pools and Executors
52.	What is a thread pool in Java?
53.	What is the Executor framework?
54.	What are the advantages of using thread pools?
55.	What is the difference between Executor, ExecutorService, and ScheduledExecutorService?
56.	What are Callable and Future interfaces?
57.	How do you shut down an executor?
________________________________________
✅ 9. Advanced Concurrency (java.util.concurrent)
58.	What is the ConcurrentHashMap?
59.	What is CopyOnWriteArrayList?
60.	What is CountDownLatch?
61.	What is CyclicBarrier?
62.	What is Semaphore?
63.	What is ReentrantLock?
64.	Difference between ReentrantLock and synchronized?
65.	What is ReadWriteLock?
66.	What is BlockingQueue?
67.	What is ThreadLocal?
________________________________________
✅ 10. Miscellaneous and Best Practices
68.	Can a thread be restarted once it has completed?
69.	What is the difference between ThreadGroup and ExecutorService?
70.	Can we forcibly stop a thread?
71.	Why is stop(), suspend(), and resume() deprecated?
72.	How to implement thread-safe singleton in Java?
73.	What are some best practices for writing multithreaded code?
74.	How do you test multithreaded applications?
________________________________________
✅ 1. Basics of Collections Framework
1.	What is the Java Collections Framework?
2.	What are the benefits of using Collections in Java?
3.	What are the main interfaces in the Collections Framework?
4.	Difference between Collection and Collections?
5.	What is the root interface of the Collections Framework?
6.	What is the difference between Iterable and Collection?
________________________________________
✅ 2. List Interface
7.	What is a List in Java?
8.	What are the implementations of the List interface?
9.	Difference between ArrayList and LinkedList?
10.	How does ArrayList work internally?
11.	What is the initial capacity of an ArrayList?
12.	How does LinkedList work internally?
13.	When to use ArrayList vs LinkedList?
14.	What is a Vector? How is it different from ArrayList?
15.	What is a Stack and how is it different from other Lists?
________________________________________
✅ 3. Set Interface
16.	What is a Set in Java?
17.	What are the implementations of Set?
18.	Difference between Set and List?
19.	What is a HashSet?
20.	How does HashSet work internally?
21.	Why doesn’t HashSet allow duplicates?
22.	What is LinkedHashSet?
23.	What is TreeSet and how does it maintain order?
24.	What is the time complexity of basic operations in HashSet and TreeSet?
________________________________________
✅ 4. Map Interface
25.	What is a Map in Java?
26.	What are the implementations of Map?
27.	Difference between HashMap and Hashtable?
28.	How does HashMap work internally (with hashCode and equals)?
29.	What is the load factor and threshold in HashMap?
30.	How does HashMap handle collisions?
31.	What is LinkedHashMap?
32.	What is TreeMap?
33.	Difference between TreeMap and HashMap?
34.	What is a ConcurrentHashMap?
35.	Can a Map have null keys or null values?
36.	What is the difference between Map and ConcurrentMap?
________________________________________
✅ 5. Queue and Deque
37.	What is a Queue in Java?
38.	What is the difference between Queue and Stack?
39.	What are PriorityQueue and its internal working?
40.	What is a Deque?
41.	What is the difference between ArrayDeque and LinkedList?
________________________________________
✅ 6. Algorithms and Utilities
42.	What are utility classes in the Collections Framework?
43.	What is the use of Collections class?
44.	What are commonly used methods in Collections?
45.	How do you sort a list in Java?
46.	How do you make a collection read-only?
47.	How to make a collection thread-safe?
48.	What is the Arrays utility class?
________________________________________
✅ 7. Iterator and ListIterator
49.	What is an Iterator in Java?
50.	Difference between Iterator and ListIterator?
51.	What is the difference between fail-fast and fail-safe iterators?
52.	Can we modify a collection while iterating?
________________________________________
✅ 8. Comparable and Comparator
53.	What is the difference between Comparable and Comparator?
54.	When to use Comparable and when to use Comparator?
55.	Can a class implement both Comparable and Comparator?
________________________________________
✅ 9. Synchronization and Thread-Safety
56.	Are Java collections thread-safe?
57.	Difference between synchronized collection and concurrent collection?
58.	What is Collections.synchronizedList()?
59.	What is CopyOnWriteArrayList?
60.	What is ConcurrentHashMap and how is it different from Hashtable?
________________________________________
✅ 10. Performance and Internal Working
61.	What is the time complexity of basic operations in List, Set, and Map implementations?
62.	How does Java resolve hash collisions in HashMap?
63.	What is the role of equals() and hashCode() in collections?
64.	How to override hashCode() and equals() properly?
65.	Why is it important to override hashCode() when overriding equals()?
________________________________________
✅ 11. Special Collections
66.	What is EnumSet?
67.	What is EnumMap?
68.	What is IdentityHashMap?
69.	What is WeakHashMap and its use case?
70.	What is Properties class in Java?
________________________________________
✅ 12. Real-Time and Practical Use
71.	When would you use a HashMap in a real-world application?
72.	How to sort a HashMap by values?
73.	How to remove duplicates from a List using Set?
74.	How do you design a custom collection class?
75.	How do you traverse a Map?
________________________________________
✅ 1. Basics of Exception Handling
1.	What is an exception in Java?
2.	What is the difference between error and exception?
3.	What is the base class for all exceptions in Java?
4.	What is the purpose of exception handling?
5.	What are the benefits of exception handling?
________________________________________
✅ 2. Types of Exceptions
6.	What are the types of exceptions in Java?
7.	What is a checked exception?
8.	What is an unchecked exception?
9.	Difference between checked and unchecked exceptions?
10.	Examples of checked exceptions in Java?
11.	Examples of unchecked exceptions in Java?
12.	What is a runtime exception?
________________________________________
✅ 3. Exception Hierarchy
13.	Explain the Java Exception class hierarchy.
14.	What is the difference between Throwable, Exception, and Error?
15.	Can we catch Error in Java?
________________________________________
✅ 4. try-catch-finally
16.	What is the syntax of try-catch?
17.	Can we use multiple catch blocks?
18.	Can we catch multiple exceptions in a single catch block (multi-catch)?
19.	Can finally block be skipped?
20.	What happens if an exception is thrown in finally block?
21.	What is the purpose of the finally block?
22.	Can we have a try block without catch or finally?
23.	Can a catch block catch more than one type of exception?
________________________________________
✅ 5. throw and throws
24.	What is the throw keyword in Java?
25.	What is the throws keyword in Java?
26.	Difference between throw and throws?
27.	Can we throw multiple exceptions using throw?
28.	Can we declare multiple exceptions using throws?
29.	Can a subclass override a method and throw a different exception?
________________________________________
✅ 6. Custom Exceptions
30.	How do you create a custom exception in Java?
31.	Should custom exceptions extend Exception or RuntimeException?
32.	What are the use cases of custom exceptions?
________________________________________
✅ 7. Exception Propagation and Chaining
33.	What is exception propagation in Java?
34.	What is exception chaining?
35.	How to chain exceptions using constructors?
36.	Can exceptions be nested?
________________________________________
✅ 8. Common Exceptions
37.	What is NullPointerException?
38.	What is ArrayIndexOutOfBoundsException?
39.	What is ClassCastException?
40.	What is NumberFormatException?
41.	What is IllegalArgumentException?
42.	What is ArithmeticException?
________________________________________
✅ 9. Best Practices
43.	What are the best practices for exception handling?
44.	Why should you avoid catching generic Exception?
45.	Is it good practice to log and throw exceptions?
46.	Should you use exceptions for flow control?
________________________________________
✅ 10. Advanced Topics
47.	Can we rethrow an exception in Java?
48.	What is suppressed exception in Java?
49.	What is the difference between final, finally, and finalize()?
50.	What is the try-with-resources statement?
51.	What interfaces must an object implement for try-with-resources?
52.	How are exceptions handled in threads?
53.	What is the Thread.UncaughtExceptionHandler?
________________________________________
✅ 11. Interview Scenarios & Tricky Questions
54.	What happens when an exception is thrown inside a catch block?
55.	Can we have multiple finally blocks?
56.	Can we return from finally block?
57.	Can we throw an exception from finally block?
58.	What happens if an exception is thrown in both catch and finally?
59.	What is the output if try has return, and finally also has return?
________________________________________
✅ 1. Overview of Java 8
1.	What are the major features introduced in Java 8?
2.	Why was Java 8 an important release?
3.	What is the default method in interfaces?
4.	What is a functional interface?
5.	What is the @FunctionalInterface annotation?
________________________________________
✅ 2. Lambda Expressions
6.	What is a lambda expression?
7.	What is the syntax of a lambda expression?
8.	How do lambda expressions improve Java programming?
9.	Can lambda expressions access local variables?
10.	What is effectively final variable?
11.	Difference between anonymous inner class and lambda expression?
12.	Can lambda expressions throw checked exceptions?
13.	Can lambda expressions have multiple statements?
________________________________________
✅ 3. Functional Interfaces
14.	What are functional interfaces provided by Java 8?
15.	What is the Predicate interface?
16.	What is the Function interface?
17.	What is the Supplier interface?
18.	What is the Consumer interface?
19.	What is the UnaryOperator and BinaryOperator interface?
20.	Can you create your own functional interface?
________________________________________
✅ 4. Streams API
21.	What is a Stream in Java 8?
22.	Difference between Collection and Stream?
23.	What are the stages of a stream pipeline?
24.	What is intermediate operation and terminal operation?
25.	How does lazy evaluation work in streams?
26.	How do you create a stream?
27.	What is the difference between sequential and parallel streams?
28.	What are some common stream operations? (filter, map, reduce, collect)
29.	How does the map() operation work?
30.	What is flatMap()?
31.	What is the purpose of reduce()?
32.	How do you convert a Stream back to a Collection?
33.	What is a Collector in Java 8 streams?
________________________________________
✅ 5. Optional Class
34.	What is Optional in Java 8?
35.	Why was Optional introduced?
36.	How to create an Optional object?
37.	What methods does Optional provide to avoid null checks?
38.	Difference between orElse(), orElseGet(), and orElseThrow()?
39.	Can Optional be used with collections?
________________________________________
✅ 6. Date and Time API
40.	What problems does the new Date and Time API solve?
41.	What are the main packages/classes introduced for date and time?
42.	What is LocalDate, LocalTime, LocalDateTime?
43.	How is the new Date-Time API better than the old java.util.Date and Calendar?
44.	How do you format dates in the new API?
45.	What is Period and Duration?
________________________________________
✅ 7. Method References
46.	What is a method reference?
47.	What are the types of method references?
48.	Difference between lambda expression and method reference?
49.	Can method references be used with constructors?
________________________________________
✅ 8. Default and Static Methods in Interfaces
50.	Why were default methods introduced?
51.	How do default methods help with backward compatibility?
52.	Can you override default methods in implementing classes?
53.	Can interfaces have static methods? How do you call them?
________________________________________
✅ 9. Parallelism and Concurrency Enhancements
54.	How does Java 8 improve parallelism?
55.	How to create parallel streams?
56.	What are the considerations when using parallel streams?
________________________________________
✅ 10. Miscellaneous Java 8 Features
57.	What are repeated annotations?
58.	What is type annotation?
59.	How do you use CompletableFuture?
60.	What are the improvements in Nashorn JavaScript engine?
________________________________________
✅ 1. Basics of Spring Boot
1.	What is Spring Boot?
2.	How is Spring Boot different from the Spring Framework?
3.	What are the main features of Spring Boot?
4.	What is the purpose of the @SpringBootApplication annotation?
5.	What is auto-configuration in Spring Boot?
6.	How does Spring Boot simplify application development?
7.	What is the Spring Boot starter?
8.	What are Spring Boot Starters? Can you name a few common starters?
9.	What is the default port of Spring Boot application?
10.	How do you change the default port in Spring Boot?
________________________________________
✅ 2. Spring Boot Architecture
11.	How does Spring Boot auto-configuration work internally?
12.	What is SpringApplication class?
13.	What is Spring Boot CLI?
14.	What is the difference between Spring Boot and Spring MVC?
15.	What is the Spring Boot actuator?
________________________________________
✅ 3. Spring Boot Annotations
16.	What is the use of @EnableAutoConfiguration?
17.	What is the difference between @Component, @Service, @Repository, and @Controller?
18.	What does @RestController do?
19.	What is the role of @ConfigurationProperties?
20.	What is @Value annotation used for?
21.	Explain @Conditional annotations in Spring Boot.
________________________________________
✅ 4. Spring Boot Configuration
22.	What are the ways to configure Spring Boot application?
23.	What is application.properties or application.yml file?
24.	How do you externalize configuration in Spring Boot?
25.	How to use profiles in Spring Boot?
26.	What is the default profile in Spring Boot?
27.	How to set active profiles?
28.	What are the different property sources Spring Boot supports?
________________________________________
✅ 5. Spring Boot Data Access
29.	What is Spring Data JPA?
30.	How do you configure a database connection in Spring Boot?
31.	How does Spring Boot manage transactions?
32.	What is the difference between CrudRepository and JpaRepository?
33.	How to perform pagination and sorting in Spring Data JPA?
34.	How to execute native queries in Spring Data JPA?
________________________________________
✅ 6. Spring Boot Security
35.	What is Spring Security?
36.	How to secure Spring Boot applications?
37.	How do you configure basic authentication in Spring Boot?
38.	What is OAuth2 in Spring Boot?
39.	How to implement JWT authentication in Spring Boot?
________________________________________
✅ 7. Spring Boot REST API
40.	How do you create a RESTful API in Spring Boot?
41.	What annotations are used to handle HTTP requests?
42.	How to handle exceptions in Spring Boot REST API?
43.	How do you enable CORS in Spring Boot?
44.	What is HATEOAS?
45.	How to test Spring Boot REST APIs?
________________________________________
✅ 8. Spring Boot Actuator
46.	What is Spring Boot Actuator?
47.	What are some useful actuator endpoints?
48.	How to customize actuator endpoints?
49.	How to secure actuator endpoints?
________________________________________
✅ 9. Spring Boot Testing
50.	How to test a Spring Boot application?
51.	What is @SpringBootTest annotation?
52.	How to write unit tests for controllers and services?
53.	How do you use MockMvc in Spring Boot?
________________________________________
✅ 10. Spring Boot Deployment
54.	How do you package a Spring Boot application?
55.	What is the difference between jar and war packaging?
56.	How to deploy Spring Boot applications in a server?
57.	What is the embedded server in Spring Boot?
58.	How to configure logging in Spring Boot?
________________________________________
✅ 11. Advanced Topics
59.	What is Spring Boot starter parent?
60.	How to create custom starters in Spring Boot?
61.	What is Spring Boot DevTools?
62.	What is the difference between @Bean and @Component?
63.	How to enable asynchronous processing in Spring Boot?
64.	How do you implement caching in Spring Boot?



