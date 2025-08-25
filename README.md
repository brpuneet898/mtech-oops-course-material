# Material for Object Oriented Programming Course(MTech 2025)

## Course Code - MA5741

This repository contains the material for the Object Oriented Programming course for MTech 2025. The course is designed to provide students with a comprehensive understanding of object-oriented programming concepts and principles. The subject was taught by Prof. Neelesh S. Upadhye at IIT Madras and delivered in July 2025 semester for MTech students.

**Note** - The reading material prepared for each week is available. It is strictly meant for course-use only. Please do not share it outside the course context or redistribute it without permission.

## Week 1

- **Content** - Python Refresher, Virtual Environments, Type Hints
- **Lab Component** - Set‑up: small coding kata
- **Reading Material** - Ramalho Ch. 1-4

## Week 2

- **Content** - Objects and Namespaces, `__init__` and `__str__`
- **Lab Component** - Design Point, Vector classes
- **Reading Material** - Exercises 1‑3

## Week 3

- **Content** - Encapsulation, properties, composition vs. inheritance
- **Lab Component** - Refactor Week‑2 code; unit tests with `pytest`
- **Reading Material** - Freeman Ch. 1-2

## Week 4

- **Content** - SOLID principles, UML class diagrams
- **Lab Component** - Draw UML from given repo; start TDD cycle
- **Reading Material** - Freeman Ch. 3, Short blog excerpt (Kent C. Dodds), Class diagram of a simple Invoice aggregate ⟷ five pytest functions

## Week 5

- **Content** - Algorithm analysis, linear & binary search
- **Lab Component** - Implement & benchmark searches
- **Reading Material** - Dasgupta Ch. 1.1-1.2

## Week 6

- **Content** - Insertion & selection sort
- **Lab Component** - Time‑plots with matplotlib
- **Reading Material** - Kleinberg Ch. 2

## Week 7

- **Content** - Merge‑ & quicksort; Timsort idea
- **Lab Component** - Refactor list sorter as strategy pattern
- **Reading Material** - Goodrich Ch. 12, Inside the CPython Timsort (Tim Peters blog), Ramalho Ch 18, 2-page handout: strategy pattern refactor of a sorter

## Week 8

- **Content** - Stacks, queues, deques
- **Lab Component** - Generic stack/queue class w/ type hints
- **Reading Material** - Goodrich Ch. 6, Ramalho Ch 6, PEP 585 summary, Short Summary on “Python Generics in Practice”, 2-page mini-exercise: design a Deque class with generics

## Week 9

- **Content** - Trees: BST & AVL; heaps, priority queues
- **Lab Component** - Implement BST, AVL, MinHeap, MaxHeap, and a job scheduler using heaps - mini project
- **Reading Material** - Goodrich Ch. 8, Dasgupta Ch. 4, Python `heapq` HOWTO excerpt, 2-page case study: heap-based job scheduler

## Week 10

- **Content** - Graphs: BFS, DFS, topological sort
- **Lab Component** - Visualise DFS/BFS with networkx
- **Reading Material** - Goodrich Ch. 14.1 - 14.5, Dasgupta Ch. 4.1 - 4.3

## Week 11

- **Content** - Shortest paths (Dijkstra), MST (Prim, Kruskal)
- **Lab Component** - Path‑finding on transport graph
- **Reading Material** - Goodrich Ch. 14.6 - 14.7, Dasgupta Ch. 4.4 - 4.7

## Week 12

- **Content** - Divide‑&‑conquer; memoisation
- **Lab Component** - Karatsuba multiplication; memoised coin‑change
- **Reading Material** - Goodrich Ch. 15, Dasgupta Ch. 2, Kleinberg Ch. 5

## Week 13

- **Content** - Dynamic programming (LIS, knapsack)
- **Lab Component** - Profiling & optimisation with cProfile
- **Reading Material** - Dasgupta Ch. 6, Kleinberg Ch. 6

## Week 14

- **Content** - Concurrency (asyncio, multiprocessing); packaging & CI
- **Lab Component** - Peer code‑review; capstone demos (No specific lab component under Week 14.)
- **Reading Material** - Ramalho Ch. 19 - 21

## Capstone Project

- `project_scope.md` - Defines the scope and deliverables for the capstone project, which involves applying advanced data structures and algorithms to solve a real-world problem.

## Extra Reference Material

- **log-log plot** - A log-log plot is a graphical representation where both axes are on a logarithmic scale. It is often used to visualize relationships between variables that span several orders of magnitude, such as the number of comparisons in binary search versus input size.
- **Solid Principles Cheatsheet** - SOLID is an acronym for five design principles intended to make software designs more understandable, flexible, and maintainable. The principles are:
  - **S**: Single Responsibility Principle
  - **O**: Open/Closed Principle
  - **L**: Liskov Substitution Principle
  - **I**: Interface Segregation Principle
  - **D**: Dependency Inversion Principle

## Quiz 1

- **Syllabus** - Week 1 to Week 3
- `quiz1_bank.md` - Contains a bank of questions for Quiz 1, covering topics such as Python virtual environments, iteration protocols, encapsulation, SOLID principles, and algorithm analysis.

## Textbook and References

### Core Text

- Goodrich, Tamassia & Goldwasser, Data Structures and Algorithms in Python

### References

- Jon Kleinberg & Éva Tardos, Algorithm Design
- Sanjoy Dasgupta, Christos Papadimitriou & Umesh Vazirani, Algorithms
- Luciano Ramalho, Fluent Python
- Steve Freeman & Nat Pryce, Growing Object-Oriented Software, Guided by Tests
