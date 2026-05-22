# OOP Interview Questions Bank
Comprehensive Object-Oriented Programming interview preparation guide## Topics Covered
OOP Fundamentals
 Inheritance & Polymorphism
 Encapsulation & Abstraction
 Design Patterns
 Interface


---

## OOP Interview Questions

### Q1: What is Inheritance?
**Answer:** Child class parent class ke features use kar sakti hai.

**Code Example:**
```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Woof!");
    }
}

** Code Example 
// Interface 1 - defines what a payable entity must do
interface Payable {
    void processPayment(double amount);  // no body, just a rule
    
    default void showReceipt() {         // has a body, free for all implementing classes
        System.out.println("Payment processed!");
    }
}

// Interface 2 - defines what a refundable entity must do
interface Refundable {
    void processRefund(double amount);   // no body, just a rule
}

// CreditCard class must follow rules of BOTH interfaces
class CreditCard implements Payable, Refundable {
    
    private String cardNumber;  // stores the card number
    
    // constructor - runs when object is created
    public CreditCard(String cardNumber) {
        this.cardNumber = cardNumber;  // assigns passed value to the field
    }
    
    // implementing Payable's rule - must provide a body here
    @Override
    public void processPayment(double amount) {
        System.out.println("Credit card " + cardNumber + " charged Rs." + amount);
    }
    
    // implementing Refundable's rule - must provide a body here
    @Override
    public void processRefund(double amount) {
        System.out.println("Rs." + amount + " refunded to card.");
    }
}

public class Main {
    public static void main(String[] args) {
        
        CreditCard card = new CreditCard("1234-5678");  // create object
        
        card.processPayment(500.0);  // calls our overridden method → prints charge message
        card.processRefund(100.0);   // calls our overridden method → prints refund message
        card.showReceipt();          // comes directly from Payable interface → prints "Payment processed!"
    }
}

## How to Use
1. Download PDF
2. Solve all questionsss
3. Master OOP concepts

---
Made by Md Rashid | May 2026
