# Week 7 Lab Evaluation Metrics – Strategy Pattern + Sorting

This document defines the evaluation criteria for assessing submissions to the **Week7_Lab.ipynb** assignment. Total score: **100 points**

## Section-wise Breakdown

### 1. SortStrategy Interface & Sorter Class (15 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| `SortStrategy` abstract base class defined properly with `sort()` method | 5      |
| `Sorter` class uses composition correctly (strategy object)              | 5      |
| Strategy swapping (`set_strategy`) works and is tested                   | 5      |

### 2. MergeSortStrategy Implementation (15 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| Recursive merge sort logic implemented correctly   | 5      |
| Stable and correct merging logic                   | 5      |
| Handles edge cases (empty list, duplicates, sorted input) | 5  |

### 3. QuickSortStrategy Implementation (15 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| Recursive quick sort with correct partitioning     | 5      |
| Handles duplicates and worst-case scenarios        | 5      |
| Returns new sorted list (no in-place mutation unless intended) | 5  |

### 4. TimSort-Inspired Strategy (25 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| Uses insertion sort for small runs                 | 5      |
| Correctly merges runs using merge logic            | 5      |
| Run size parameterized and scalable                | 5      |
| Efficient implementation (not brute force)         | 5      |
| Overall hybrid sorting correctness and stability   | 5      |

### 5. Strategy Pattern with Key Function Support (10 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| `sort(data, key=...)` implemented in all strategies | 5     |
| Custom key-based sorting (e.g., on dict fields) works | 5     |

### 6. Real-World Scenario: Log Sorter (10 points)

| Criteria                                           | Points |
|----------------------------------------------------|--------|
| Successfully sorts logs based on timestamp, level, and message length | 5 |
| Code readability, clarity of key function use      | 5      |

## Final Notes

- Encourage students to test on diverse inputs (large, reverse sorted, all equal elements, etc.).
- Focus on **correctness, OOP design, reusability**, and **real-world adaptability**.
- Give partial credit if the logic is present but not fully working.
