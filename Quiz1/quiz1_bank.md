# Quiz 1 Bank

## Part 1: Questions

---

### Multiple Choice Questions (10)

**Q1.** What is the purpose of a Python virtual environment?  
a) To make Python run faster  
b) To isolate project dependencies  
c) To encrypt source code  
d) To compile Python to C  

**Q2.** Given the following class, which change will allow it to be used in a for-loop?

```python
class Counter:
    def __init__(self, low, high):
        self.current = low
        self.high = high
```

a) Add a `__call__` method  
b) Add `__iter__` and `__next__` methods  
c) Add a `__str__` method  
d) Add a `__getitem__` method

**Q3.** Which code will ensure that `print(obj)` outputs "Hello" for the following class?

```python
class MyClass:
    pass

obj = MyClass()
print(obj)
```

a) Add a `def __repr__(self): return "Hello"` method  
b) Add a `def __add__(self, other): return "Hello"` method  
c) Add a `def __str__(self): return "Hello"` method  
d) Add a `def __init__(self): print("Hello")` method

**Q4.** What is the difference between immutable and mutable sequences in Python?  
a) Immutable sequences cannot be iterated  
b) Immutable sequences can change size  
c) Immutable sequences cannot be changed after creation  
d) Mutable sequences are faster

**Q5.** What does LEGB stand for in Python namespaces?  
a) Local, External, Global, Built-in  
b) Local, Enclosing, Global, Built-in  
c) Loop, Encapsulation, Global, Base  
d) List, Expression, Global, Base

**Q6.** Which of these correctly describes the role of `__init__`?  
a) Allocates memory for new objects  
b) Initializes the object after allocation  
c) Deletes objects  
d) Returns the object ID

**Q7.** Which method in a class is used for operator overloading for addition?  
a) `__eq__`  
b) `__str__`  
c) `__add__`  
d) `__call__`

**Q8.** Which is true about encapsulation in OOP?  
a) It hides the internal state of objects  
b) It breaks modularity  
c) It always requires public attributes  
d) It makes code less maintainable

**Q9.** When should inheritance be preferred over composition?  
a) When runtime flexibility is needed  
b) When there is a clear "is-a" relationship  
c) When delegation is required  
d) When you want to avoid tight coupling

**Q10.** What does the Liskov Substitution Principle (LSP) state?  
a) Subclasses must be private  
b) Subclasses must override all methods  
c) Subclasses must be replaceable for their base classes  
d) Subclasses must use composition

---

### Short Answer Questions (5)

**SA1.** Explain the role of Python type hints.  

**SA2.** Differentiate between `__repr__` and `__str__` methods.  

**SA3.** Describe the LEGB rule with an example.  

**SA4.** What is the purpose of using properties (getters/setters) in Python classes?  

**SA5.** Explain the difference between composition and inheritance with suitable examples.  

---

## Part 2: Answer Key with Rationales

---

### MCQ Answers

**Q1.** b) To isolate project dependencies  

> *Rationale:* Virtual environments allow each project to have its own dependencies, avoiding version conflicts and system pollution:contentReference[oaicite:0]{index=0}.

**Q2.** b) Add `__iter__` and `__next__` methods  

> *Rationale:* The iteration protocol requires implementing `__iter__` (returns iterator) and `__next__` (returns next item), enabling use in for-loops.

**Q3.** c) Add a `def __str__(self): return "Hello"` method  

> *Rationale:* Defining `__str__` customizes the output of `print(obj)` to return "Hello".

**Q4.** c) Immutable sequences cannot be changed after creation  

> *Rationale:* Immutable sequences like tuples cannot be modified once created, unlike lists:contentReference[oaicite:3]{index=3}.

**Q5.** b) Local, Enclosing, Global, Built-in  

> *Rationale:* LEGB describes Python's name resolution order:contentReference[oaicite:4]{index=4}.

**Q6.** b) Initializes the object after allocation  

> *Rationale:* `__init__` is the initializer, setting object state post-allocation:contentReference[oaicite:5]{index=5}.

**Q7.** c) `__add__`  

> *Rationale:* Used for overloading `+` operator to define custom addition behavior:contentReference[oaicite:6]{index=6}.

**Q8.** a) It hides the internal state of objects

> *Rationale:* Encapsulation prevents external access to an object's internal state, improving robustness and modularity:contentReference[oaicite:7]{index=7}.

**Q9.** b) When there is a clear "is-a" relationship  

> *Rationale:* Inheritance is ideal for "is-a" relationships, whereas composition suits "has-a" relationships:contentReference[oaicite:8]{index=8}.

**Q10.** c) Subclasses must be replaceable for their base classes  

> *Rationale:* LSP ensures subclasses can substitute for their base classes without altering program correctness:contentReference[oaicite:9]{index=9}.

---

### Short Answer Keys

**SA1.** *Explain the role of Python type hints.*  

> Type hints provide optional static typing in Python. They help with IDE support, code readability, static analysis tools (e.g., mypy) to catch errors early, but are not enforced at runtime unless checked with additional tools:contentReference[oaicite:10]{index=10}.

---

**SA2.** *Differentiate between `__repr__` and `__str__` methods.*  

> `__repr__` aims for unambiguous representations useful for debugging, while `__str__` is meant for human-friendly displays. By convention, `__str__` is used in `print()` and user interfaces:contentReference[oaicite:11]{index=11}.

---

**SA3.** *Describe the LEGB rule with an example.*  

> LEGB stands for Local, Enclosing, Global, Built-in. Example:

> ```python
> x = "global"
> def outer():
>     x = "enclosing"
>     def inner():
>         x = "local"
>         print(x)
>     inner()
> outer()
> ```  

> Output is "local" because Python searches names in this order: Local → Enclosing → Global → Built-in:contentReference[oaicite:12]{index=12}.

---

**SA4.** *What is the purpose of using properties (getters/setters) in Python classes?*  

> Properties allow controlled access to an object's internal state. Getters return the value, setters can validate or enforce invariants before updating, supporting encapsulation principles:contentReference[oaicite:13]{index=13}.

---

**SA5.** *Explain the difference between composition and inheritance with suitable examples.*  

> - **Composition:** "has-a" relationship. Example: A Car has an Engine. The Car class can use Engine’s behavior via delegation.  
> - **Inheritance:** "is-a" relationship. Example: Dog is an Animal. Dog inherits common Animal behaviors.  
> Composition promotes flexibility by swapping components; inheritance promotes reuse with polymorphic substitution but can lead to tight coupling if overused:contentReference[oaicite:14]{index=14}.
