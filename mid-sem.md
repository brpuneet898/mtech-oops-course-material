# Mid-Semester Exam

- Total Marks: 40
- Duration: 90 minutes
- There are 14 questions in total.
  - Question 1 to Question 5 are multiple-choice questions (MCQs) worth 1 mark each.
  - Question 6 to Question 10 are short answer questions worth 2 marks each.
  - Question 11 to Question 14 are long answer questions worth 5 marks each.
- Answer all questions.

## 1

Which of the following statements about Python’s virtual environments is **true**? (1 marks)

A. They globally install packages to avoid redundancy  
B. They prevent version conflicts between projects  
C. They remove the need for pip  
D. They automatically enforce type hints

Answer: B

---

## 2

In Python OOP, what is the primary purpose of the `__str__` method? (1 marks)

A. To initialize object attributes  
B. To provide a machine-readable string representation  
C. To provide a human-readable string representation  
D. To define operator overloading

Answer: C

---

## 3

Which SOLID principle states that a class should have only one reason to change? (1 marks)

A. Open-Closed Principle  
B. Single Responsibility Principle  
C. Interface Segregation Principle  
D. Dependency Inversion Principle

Answer: B

---

## 4

What is the **worst-case time complexity** of Binary Search? (1 marks)

A. O(1)  
B. O(n)  
C. O(log n)  
D. O(n log n)

Answer: C

---

## 5

Which of the following properties makes **Timsort** particularly efficient for real-world datasets? (1 marks)

A. It is always faster than Quicksort  
B. It is unstable but adaptive  
C. It combines Merge Sort and Insertion Sort to exploit runs  
D. It requires no auxiliary space

Answer: C

---

## 6

Explain the difference between **identity** and **equality** in Python objects with a suitable example. (2 marks)

---

## 7

Consider the following code snippet:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y
p1 = Point(1, 2)
p2 = Point(1, 2)
```

- What will p1 == p2 return by default?
- How can we modify the class to make p1 == p2 return True? (1 + 1 marks)

---

## 8

Differentiate between composition and inheritance in OOP. Give one example scenario where composition is preferable. (2 marks)

---

## 9

Write a Python function `binary_search(arr, key)` using iteration. Also state its time complexity in worst case. (1 + 1 marks)

---

## 10

State whether the following sorting algorithms are stable or unstable, and justify in detail:
(a) Insertion Sort
(b) Selection Sort (1 + 1 marks)

---

## 11

Discuss the **Liskov Substitution Principle (LSP)** in detail. Provide one Python example where violating LSP causes incorrect behavior. (2 + 3 marks)

---

## 12

You are asked to design a **Vector class** that supports addition, subtraction, and magnitude calculation.  
(a) Write the Python class structure with at least `__init__`, `__add__`, and `magnitude()` methods.  
(b) Explain how operator overloading improves code readability in this context. (3 + 2 marks)

---

## 13

(a) Draw and explain a **UML class diagram** for a simple e-commerce system involving `Customer`, `Order`, and `Product` classes. Show relationships (association, composition, inheritance).  
(b) Write Python code implementing `Order` containing a list of `Product` objects using **composition**. (2 + 2 + 1 marks)

---

## 14

Consider the following problem: You are given an unsorted list of integers.  
(a) Explain with reasoning why **Merge Sort** is preferred over **Quick Sort** for sorting a linked list.  
(b) Implement Merge Sort for a linked list in Python (you may assume a basic `Node` class is already defined). (2 + 3 marks)
