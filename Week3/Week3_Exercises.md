# Week 3 Exercises  
**Topic: Encapsulation, Properties, Composition, and Inheritance**

## Q1. Encapsulation and Properties 

Define a class `BankAccount` with the following requirements:  
1. Use **private attributes** `_balance` and `_owner`.  
2. Implement getter and setter properties for balance with validation (balance cannot go below `0`).  
3. Provide methods `deposit(amount)` and `withdraw(amount)` that modify the balance safely.  
4. Demonstrate why behaviour-based methods (like `deposit`) are preferred over raw setters.

*Hint*: Show what happens when direct balance manipulation is allowed vs. when encapsulation is enforced.

## Q2. Behavioural Encapsulation vs Data Exposure 

Consider a `Student` class storing `marks` for 3 subjects.  

1. Implement it with only getters/setters (data exposure).  
2. Then, re-implement it using **behavioural encapsulation**, where you add a method `calculate_grade()` that internally computes grade instead of exposing marks directly.  
3. Compare both implementations. Which design better follows the principle of *“Tell, don’t ask”*?

## Q3. Composition vs Inheritance  

Create two designs for a `Car` system:  

- **Inheritance-based**: A `Car` inherits from `Engine`.  
- **Composition-based**: A `Car` *has an* `Engine` (composition).  

1. Write minimal Python classes for both approaches.  
2. Demonstrate how composition allows easier replacement (e.g., swapping a `PetrolEngine` with an `ElectricEngine`) compared to inheritance.  
3. Conclude: In which case is composition preferable?

## Q4. Liskov Substitution Principle (LSP)  

1. Create a class `Bird` with a method `fly()`.  
2. Implement subclasses `Sparrow` (can fly) and `Penguin` (cannot fly).  
3. Show how substituting `Penguin` for `Bird` breaks LSP.  
4. Refactor the design using **composition** (e.g., `FlyBehavior`) so that LSP holds true.  

*Hint*: Think about “is-a” vs “has-a” relationship while redesigning.
