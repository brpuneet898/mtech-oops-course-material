# Week 13 – Lab Evaluation Metrics  

This document defines the **evaluation metrics** for assessing student submissions of **Week 13 Lab**.  
Each question will be graded on correctness, completeness, efficiency, and analysis.  

## Question-Wise Breakdown

### Q1. Longest Increasing Subsequence (LIS)  
- **Naïve Recursive Solution (5%)**: Correct recursive formulation, handles base cases.  
- **DP O(n²) Solution (10%)**: Proper DP table/memoisation with correct transitions.  
- **Optimised O(n log n) Solution (10%)**: Correct use of binary search (`bisect`) to achieve O(n log n).  
- **Profiling & Comparison (10%)**: `cProfile` runs on large inputs, results compared with clear observations.  
- **Discussion (5%)**: Insights into trade-offs between simplicity, runtime, and scalability.  

**Total: 40%**  

---

### Q2. 0/1 Knapsack  
- **Naïve Recursive Solution (5%)**: Correct recursion with include/exclude logic.  
- **DP with 2D Table (10%)**: Proper filling of table with correct state transitions.  
- **Space-Optimised DP (10%)**: Correct implementation with 1D array.  
- **Profiling & Memory Considerations (10%)**: Profiling outputs for each version, memory comparisons included.  
- **Discussion (5%)**: Trade-offs between time and space discussed clearly.  

**Total: 40%**  

---

### Q3. Knapsack with Dependencies (Case Study)  
- **Topological Sorting (5%)**: Correct handling of project dependencies.  
- **DP with Dependencies (10%)**: Valid knapsack implementation that respects ordering constraints.  
- **Profiling & Optimisation (10%)**: Large dataset profiling done, optimisation strategies applied.  
- **Analysis & Reflection (5%)**: Scalability analysis, discussion of bottlenecks, and real-world applicability.  

**Total: 30%**  
