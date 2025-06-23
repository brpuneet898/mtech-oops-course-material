# Week 1 Lab Evaluation Metrics

Total Marks: 100

---

## Section 1: Environment Setup and Sanity Checks (20 marks)

- **Virtual Environment Creation (5 marks)**
  - Correctly creates and activates a Python virtual environment.
- **Package Installation (5 marks)**
  - Installs required packages (`mypy`, `rich`) in the environment.
- **Sanity Script (10 marks)**
  - Script correctly prints Python interpreter path and lists installed packages.

---

## Section 2: Python Sequences & Data Model (30 marks)

- **FrenchDeck Implementation (15 marks)**
  - Implements `FrenchDeck` with correct data model methods (`__len__`, `__getitem__`, `__setitem__`, `__contains__`, `__str__`, `__repr__`).
  - Uses `namedtuple` for `Card`.
- **Idiomatic Usage (5 marks)**
  - Supports slicing, shuffling, and membership tests.
- **Unit Tests (10 marks)**
  - Provides and passes unit tests for deck length, indexing, membership, slicing, and shuffling.

---

## Section 3: Type Hints and Static Checking (20 marks)

- **Type Annotations (10 marks)**
  - Annotates `FrenchDeck` and related functions/classes with appropriate type hints.
- **Static Checking (5 marks)**
  - Runs `mypy` or similar tool and resolves all type errors.
- **Type Hint Usage Example (5 marks)**
  - Demonstrates a function using type hints (e.g., `count_suits`).

---

## Section 4: Data Model & Type Hints (30 marks)

- **Vector2D Implementation (15 marks)**
  - Implements `Vector2D` with correct dunder methods (`__init__`, `__repr__`, `__abs__`, `__add__`, `__mul__`, `__bool__`, `__eq__`).
- **Type Hints (10 marks)**
  - All methods and attributes are properly type-annotated.
- **Testing and Usage (5 marks)**
  - Demonstrates usage and correctness with sample operations and outputs.

---

## Bonus (up to 5 marks)

- **Extra Pythonic Features**
  - Implements additional idiomatic features, documentation, or error handling.

---

**Note:** Partial marks may be awarded for incomplete or partially correct
