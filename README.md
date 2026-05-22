# OOP Interview Questions Bank

A comprehensive collection of Object-Oriented Programming interview questions and answers with practical code examples.

---

## Interview Questions

### Q1: What is Inheritance?

**Answer:**
Inheritance is a mechanism where a child class (derived class) inherits properties and methods from a parent class (base class). This promotes code reusability and establishes a hierarchical relationship between classes.

**Code Example:**
```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();   // Inherited from Animal
        dog.bark();  // Own method
    }
}
```

**Key Points:**
- Child class automatically gets all non-private members of parent class
- Uses `extends` keyword in Java
- Supports code reusability and method overriding

---

### Q2: What is Polymorphism?

**Answer:**
Polymorphism means "many forms". It allows objects of different classes to be treated as objects of a common parent class. There are two types: compile-time (method overloading) and runtime (method overriding).

**Code Example:**
```java
class Shape {
    void draw() {
        System.out.println("Drawing a shape");
    }
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle");
    }
}

class Square extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a square");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Square();
        
        s1.draw();  // Calls Circle's draw()
        s2.draw();  // Calls Square's draw()
    }
}
```

**Key Points:**
- Method Overloading: Same method name, different parameters (compile-time)
- Method Overriding: Same method name in parent and child class (runtime)
- Enables flexible and extensible code

---

### Q3: What is Encapsulation?

**Answer:**
Encapsulation is the bundling of data (variables) and methods into a single unit called a class. It restricts direct access to an object's internal data and provides controlled access through public methods (getters and setters).

**Code Example:**
```java
class BankAccount {
    private int balance;  // Private data - cannot be accessed directly
    
    public BankAccount(int initialBalance) {
        this.balance = initialBalance;
    }
    
    public int getBalance() {
        return balance;
    }
    
    public void deposit(int amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: " + amount);
        }
    }
    
    public void withdraw(int amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: " + amount);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount account = new BankAccount(1000);
        account.deposit(500);    // Only through method
        account.withdraw(200);   // Validated withdrawal
        System.out.println("Balance: " + account.getBalance());
    }
}
```

**Key Points:**
- Data hiding: Private variables cannot be accessed directly
- Controlled access: Public methods validate data before modification
- Increases security and maintains data integrity
- Improves maintainability

---

### Q4: What is Abstraction?

**Answer:**
Abstraction is the process of hiding complex implementation details and showing only the essential features. Abstract classes and interfaces are used to achieve abstraction.

**Code Example:**
```java
abstract class Vehicle {
    abstract void start();
    abstract void stop();
    
    void honk() {
        System.out.println("Vehicle honking");
    }
}

class Car extends Vehicle {
    @Override
    void start() {
        System.out.println("Car engine starting");
    }
    
    @Override
    void stop() {
        System.out.println("Car engine stopping");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle car = new Car();
        car.start();  // Uses implemented method
        car.honk();   // Uses inherited method
        car.stop();
    }
}
```

**Key Points:**
- Abstract classes cannot be instantiated
- Must implement all abstract methods in concrete class
- Provides a blueprint for subclasses

---

## Topics Covered

✅ Inheritance - Code reusability and hierarchy
✅ Polymorphism - Flexibility and extensibility
✅ Encapsulation - Data protection and validation
✅ Abstraction - Hiding complexity

---

## How to Use This Guide

1. Review each question carefully
2. Understand the concept before looking at code
3. Try implementing the examples yourself
4. Practice explaining these concepts verbally
5. Use these as interview preparation material

---

## Interview Tips

- Explain concepts with real-world analogies
- Always provide code examples when possible
- Discuss advantages and disadvantages of each concept
- Ask clarifying questions if needed
- Practice coding the examples from scratch

---

Made by Md Rashid | May 2026
