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

<img src="./Java Crash Course/Java Crash Course-001.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-002.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-003.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-004.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-005.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-006.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-007.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-008.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-009.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-010.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-011.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-012.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-013.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-014.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-015.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-016.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-017.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-018.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-019.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-020.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-021.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-022.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-023.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-024.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-025.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-026.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-027.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-028.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-029.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-030.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-031.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-032.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-033.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-034.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-035.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-036.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-037.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-038.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-039.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-040.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-041.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-042.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-043.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-044.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-045.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-046.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-047.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-048.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-049.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-050.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-051.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-052.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-053.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-054.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-055.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-056.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-057.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-058.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-059.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-060.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-061.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-062.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-063.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-064.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-065.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-066.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-067.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-068.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-069.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-070.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-071.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-072.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-073.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-074.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-075.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-076.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-077.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-078.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-079.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-080.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-081.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-082.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-083.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-084.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-085.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-086.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-087.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-088.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-089.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-090.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-091.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-092.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-093.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-094.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-095.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-096.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-097.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-098.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-099.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-100.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-101.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-102.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-103.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-104.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-105.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-106.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-107.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-108.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-109.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-110.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-111.png" width="1920" />
<img src="./Java Crash Course/Java Crash Course-112.png" width="1920" />

