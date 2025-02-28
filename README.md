# JAVA Course for beginners
Java is a versatile, object-oriented programming language widely used for building enterprise-scale applications, mobile apps (Android), web applications, and more. Below, I’ll provide a sort of "all-in-one" Java guide with examples covering basic syntax, sorting algorithms, and Object-Oriented Programming (OOP) concepts.

## 1. Basic Java Syntax
### Hello World Program
```cs
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
## 2. Sorting Algorithms in Java
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
## 3. Object-Oriented Programming (OOP) Concepts
### Classes and Objects
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
### Inheritance
```cs
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("The cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Cat myCat = new Cat();
        myCat.eat(); // Inherited from Animal
        myCat.meow(); // Specific to Cat
    }
}
```
### Polymorphism (Method Overriding)
```cs
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog(); // Upcasting
        myAnimal.sound(); // Output: Dog barks
    }
}
```
### Encapsulation
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
### Abstraction (Using Abstract Class)
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
### interfaces :
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
## 4. Collections Framework
### ArrayList Example
```cs
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");

        System.out.println("Fruits: " + fruits);
    }
}
```
### HashMap Example
```cs
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> map = new HashMap<>();
        map.put("Alice", 25);
        map.put("Bob", 30);

        System.out.println("Bob's age: " + map.get("Bob")); // Output: Bob's age: 30
    }
}
```
## 5. Exception Handling
```cs
public class Main {
    public static void main(String[] args) {
        try {
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exception caught: " + e.getMessage());
        } finally {
            System.out.println("This will always execute.");
        }
    }
}
```
## 6. File Handling
### Reading a File
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
# Exceptions:
## Types of Exceptions:

### 1. Checked Exceptions: 
These are exceptions that are checked at compile-time. For example, IOException and SQLException.

### 2. Unchecked Exceptions: 
These are exceptions that are checked at runtime. For example, NullPointerException and ArithmeticException.

### 3. Errors: 
These are serious problems that a reasonable application should not try to catch. For example, OutOfMemoryError and StackOverflowError.

## Key Components:

### 1. try block: The code that might throw an exception is placed inside the try block.

### 2. catch block: This block catches and handles the exception.

### 3. finally block: This block executes regardless of whether an exception occurred or not. It's typically used for resource cleanup.

### 4. throw keyword: Used to explicitly throw an exception.

### 5. throws keyword: Used in method signatures to declare the exceptions that a method can throw.
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
### 3. finally Block
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

