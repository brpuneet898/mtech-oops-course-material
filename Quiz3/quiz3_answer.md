# Quiz 3 (DP and Concurrency)

- Name: 
- Roll Number:

## Instructions

- Maximum Marks: 10
- Duration: 1 hour
- Section A consists of 5 MCQ Questions.
- Section B consists of 5 NAT-based Questions. 
- Each questions carries 1 marks. 
- All questions are compulsory. 

## Section A [MCQ]

**Q1:** Which of the following best differentiates concurrency from parallelism?

- A. Concurrency means executing multiple tasks simultaneously.
- B. Concurrency means managing multiple tasks, not necessarily at the same instant.
- C. Parallelism means managing tasks without simultaneous execution.
- D. Concurrency requires multiple CPU cores.

Answer: B
Explanation: Concurrency focuses on task management and coordination, while parallelism is about simultaneous execution on multiple cores.

---

**Q2:** In Python, the Global Interpreter Lock (GIL) limits parallel execution in:

- A. multiprocessing
- B. asyncio
- C. threading
- D. subprocess

Answer: C
Explanation: The GIL prevents true parallelism for CPU-bound tasks in threading, though multiprocessing avoids it via separate interpreters.

---

**Q3:** Which concurrency model is most suitable for network I/O-bound workloads?

- A. Threading
- B. Multiprocessing
- C. Asyncio
- D. Sequential loops

Answer: C
Explanation: asyncio’s event-loop + coroutines enable non-blocking I/O, ideal for thousands of connections.

---

**Q4:** In Python’s multiprocessing module, processes communicate via —

- A. Global variables
- B. Shared lists directly
- C. Queues or Pipes
- D. Locks and Semaphores only

Answer: C
Explanation: Each process has isolated memory; data exchange uses IPC mechanisms like Queues, Pipes or Shared Memory.

---

**Q5:** Which of the following statements about Concurrency Trade-offs is TRUE?

- A. asyncio is best for CPU-bound tasks.
- B. threading avoids the GIL entirely.
- C. multiprocessing uses more memory but achieves true parallelism.
- D. All models share the same memory space.

Answer: C
Explanation: multiprocessing duplicates interpreters → higher RAM cost but real parallel CPU usage.

---

## Section B

```python
arr = [3, 10, 2, 1, 20]
dp = [1]*len(arr)
for i in range(1, len(arr)):
    for j in range(i):
        if arr[i] > arr[j]:
            dp[i] = max(dp[i], dp[j]+1)
print(max(dp))
```

**Q6:** What value is printed?

Ans:

Answer: 3
Explanation: LIS = [3, 10, 20] → length 3.

---

```python
val = [60, 100, 120]
wt  = [10, 20, 30]
W = 50
dp = [[0]*(W+1) for _ in range(len(val)+1)]
for i in range(1, len(val)+1):
    for w in range(1, W+1):
        if wt[i-1] <= w:
            dp[i][w] = max(val[i-1]+dp[i-1][w-wt[i-1]], dp[i-1][w])
        else:
            dp[i][w] = dp[i-1][w]
print(dp[len(val)][W])
```

**Q7:** What final value does `dp[3][50]` store?

Ans:

Answer: 220
Explanation: Optimal = items 2 & 3 → 100 + 120 = 220.

---

```python
val = [10, 30, 20]
wt  = [5, 10, 15]
W = 20
dp = [0]*(W+1)
for i in range(len(val)):
    for w in range(wt[i], W+1):
        dp[w] = max(dp[w], val[i]+dp[w-wt[i]])
print(dp[W])
```

**Q8:** What is the printed result?

Ans:

Answer: 60
Explanation: Two × 10-weight items = 60 (max value ≤ 20 weight).

---

```python
arr = [5, 8, 3, 7, 9, 1]
dp = [1]*len(arr)
for i in range(len(arr)):
    for j in range(i):
        if arr[i] > arr[j]:
            dp[i] = max(dp[i], dp[j]+1)
print(max(dp))
```

**Q9:** Output value?

Ans:

Answer: 3
Explanation: One LIS is [5, 7, 9] (length 3).

---

```python
val = [20, 5, 10, 40, 15, 25]
wt  = [1, 2, 3, 8, 7, 4]
W = 10
n = len(val)
dp = [[0]*(W+1) for _ in range(n+1)]
for i in range(1, n+1):
    for w in range(1, W+1):
        if wt[i-1] <= w:
            dp[i][w] = max(val[i-1]+dp[i-1][w-wt[i-1]], dp[i-1][w])
        else:
            dp[i][w] = dp[i-1][w]
print(dp[n][W])
```

**Q10:** What value is printed?

Ans:

Answer: 60
Explanation: Best combo = items 1 + 3 + 6 → 20 + 10 + 25 = 55 or items 1 + 4 = 60 (max).

---