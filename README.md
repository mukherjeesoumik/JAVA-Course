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
