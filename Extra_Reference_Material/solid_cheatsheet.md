# SOLID Principles Cheatsheet

The SOLID principles are five design principles intended to make object-oriented designs more understandable, flexible, and maintainable.

---

## S — Single Responsibility Principle (SRP)

**Definition**: A class should have only one reason to change.

**Explanation**: Each class should focus on a single task or responsibility.

**Example**:

```java
// Bad
class Report {
    void generate() { /* ... */ }
    void print() { /* ... */ }
}

// Good
class ReportGenerator {
    void generate() { /* ... */ }
}

class ReportPrinter {
    void print() { /* ... */ }
}
```

---

## O — Open/Closed Principle (OCP)

**Definition**: Software entities should be open for extension but closed for modification.

**Explanation**: You should be able to add new functionality without changing existing code.

**Example**:

```java
// Bad
class DiscountCalculator {
    double calculate(String type) {
        if (type.equals("Regular")) return 0.1;
        if (type.equals("Premium")) return 0.2;
        return 0;
    }
}

// Good
interface Discount {
    double calculate();
}

class RegularDiscount implements Discount {
    public double calculate() { return 0.1; }
}

class PremiumDiscount implements Discount {
    public double calculate() { return 0.2; }
}
```

---

## L — Liskov Substitution Principle (LSP)

**Definition**: Subtypes must be substitutable for their base types.

**Explanation**: Objects of a superclass should be replaceable with objects of a subclass without breaking the application.

**Example**:

```java
// Violation
class Bird {
    void fly() {}
}

class Ostrich extends Bird {
    void fly() {
        throw new UnsupportedOperationException();
    }
}

// Correct
interface Bird {}

interface FlyingBird extends Bird {
    void fly();
}

class Sparrow implements FlyingBird {
    public void fly() { /* ... */ }
}

class Ostrich implements Bird {
    // No fly method, which is fine
}
```

---

## I — Interface Segregation Principle (ISP)

**Definition**: Clients should not be forced to depend on methods they do not use.

**Explanation**: Create specific interfaces instead of a large, general-purpose one.

**Example**:

```java
// Bad
interface Worker {
    void work();
    void eat();
}

// Good
interface Workable {
    void work();
}

interface Eatable {
    void eat();
}

class Robot implements Workable {
    public void work() { /* ... */ }
}

class Human implements Workable, Eatable {
    public void work() { /* ... */ }
    public void eat() { /* ... */ }
}
```

---

## D — Dependency Inversion Principle (DIP)

**Definition**: High-level modules should not depend on low-level modules. Both should depend on abstractions.

**Explanation**: Depend on interfaces, not concrete implementations.

**Example**:

```java
// Bad
class LightBulb {
    void turnOn() { /* ... */ }
}

class Switch {
    private LightBulb bulb;

    Switch() {
        bulb = new LightBulb();
    }

    void operate() {
        bulb.turnOn();
    }
}

// Good
interface Switchable {
    void turnOn();
}

class LightBulb implements Switchable {
    public void turnOn() { /* ... */ }
}

class Switch {
    private Switchable device;

    Switch(Switchable device) {
        this.device = device;
    }

    void operate() {
        device.turnOn();
    }
}
```

---

## Solid Principles Summary

| Principle | Description |
|----------|-------------|
| **SRP**  | One class = one responsibility |
| **OCP**  | Open for extension, closed for modification |
| **LSP**  | Subclasses should be substitutable for base classes |
| **ISP**  | Use small, specific interfaces |
| **DIP**  | Depend on abstractions, not concrete implementations |

---
