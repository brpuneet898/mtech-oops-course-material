# Week 12 – Evaluation Metrics  

## Evaluation Overview
This document provides the **grading rubric** and **evaluation criteria** for assessing submissions to the **Week 12 Lab (Week12_Lab.ipynb)**.  
The lab consists of 3 core questions, and evaluation will be based on **correctness, efficiency, clarity, and analysis**.  

---

## 1. Karatsuba Multiplication (30 Marks)
**Objective**: Correctly implement the divide-and-conquer multiplication algorithm.

### Metrics:
- **Correctness (10 marks)**:  
  - Correct handling of base cases.  
  - Accurate recursive decomposition and recombination.  
  - Works for numbers up to 1000+ digits.  
- **Efficiency (5 marks)**:  
  - Implementation must show **faster runtime** than naive \(O(n^2)\) approach on large inputs.  
- **Code Design (5 marks)**:  
  - Clear modular OOP implementation (`KaratsubaMultiplier` class).  
  - Proper use of recursion and helper methods.  
- **Experimental Validation (10 marks)**:  
  - Performance comparison with Python’s `*` operator.  
  - Results demonstrated on 1000+ digit integers.  
  - Observations documented in markdown.  

---

## 2. Memoised Coin Change (30 Marks)
**Objective**: Apply memoisation to solve coin change problems efficiently.

### Metrics:
- **Correctness (10 marks)**:  
  - Correct results for both **minimum coins** and **number of ways**.  
  - Handles edge cases (e.g., target=0, target < smallest coin).  
- **Efficiency (5 marks)**:  
  - Must show significant improvement over naive recursion.  
  - Use of memoisation tables (`memo_min`, `memo_count`).  
- **Code Design (5 marks)**:  
  - Modular implementation with a `CoinChange` class.  
  - Clear separation of logic between `min_coins` and `count_ways`.  
- **Experimental Validation (10 marks)**:  
  - Comparison between recursive vs memoised performance.  
  - Testing with **large targets (5000+)** and multiple coin sets.  
  - Time/space complexity analysis included in markdown.  

---

## 3. Hybrid Challenge – Karatsuba + Coin Change (40 Marks)
**Objective**: Demonstrate integration of divide-and-conquer + memoisation in a cryptographic-inspired setting.

### Metrics:
- **Correctness (15 marks)**:  
  - Successful computation of \(N = p \times q\) using Karatsuba.  
  - Proper handling of modulus subset for feasibility.  
  - Correct results for both minimum coins and number of ways.  
- **Innovation (10 marks)**:  
  - Creative integration of two concepts.  
  - Use of first 100 primes as denominations.  
- **Code Design (5 marks)**:  
  - Object-oriented integration (`CryptoChallenge` class).  
  - Clean and modular implementation.  
- **Analysis & Discussion (10 marks)**:  
  - Observations on limitations of the approach.  
  - Practical relevance in number theory/cryptography.  
  - Reflection on why divide-and-conquer + memoisation are essential.  

---

## General Rubric (All Questions)
- **Code Quality (5 marks)**: Readability, comments, modularity.  
- **Markdown Documentation (5 marks)**: Clear explanations, experimental results, and analysis.  
