# Quiz 2 — Stacks, Queues, Deques, and Sorting

**Course:** Object Oriented Programming (MA5741)  
**Maximum Marks:** 10  
**Duration:** 30 minutes  
**Type:** MCQ & MSQ (4 options each; some single-correct, others multiple-correct)

---

### [MCQ 1]
Consider the following code fragment:

```python
def mystery_sort(A):
    for i in range(1, len(A)):
        key = A[i]
        j = i - 1
        while j >= 0 and A[j] > key:
            A[j+1] = A[j]
            j -= 1
        A[j+1] = key
    for i in range(len(A)):
        min_i = i
        for j in range(i+1, len(A)):
            if A[j] < A[min_i]:
                min_i = j
        A[i], A[min_i] = A[min_i], A[i]
```

If the input is `A = [3, 1, 2]`, which statement is **TRUE** about the number of element comparisons?

A.  Exactly 3 comparisons occur overall.  
B.  Exactly 5 comparisons occur.  
C.  Insertion phase ≈ 3 comparisons + Selection phase ≈ 3 comparisons → 6 total.  
D.  Comparisons depend on pivot selection in line 3.  

---

### [MSQ 2] 
Select **all true** statements.

A. Merge Sort is stable and guarantees O(n log n) time for all inputs.  
B. Quick Sort’s average case is O(n log n), but its worst case is O(n²).  
C. Quick Sort can be made stable by careful pivot selection.  
D. Merge Sort uses O(1) auxiliary space for array inputs.

---

### [MCQ 3]
Evaluate the output:

```python
def process(data):
    stack = []
    for ch in data:
        if ch.isupper():
            stack.append(ch.lower())
        elif ch.islower() and stack and stack[-1] == ch:
            stack.pop()
        else:
            stack.append(ch)
    return ''.join(stack)

print(process("AaBbCcDDc"))
```

A. `""` 
B. `"DDc"`
C. `"d"` 
D. `"dc"`

---

### [MSQ 4]
Given the following sequence of operations:

```python
D = empty deque
D.addRear('X')
D.addFront('Y')
D.addRear('Z')
D.removeFront()
D.addFront('W')
```

Select all correct resulting states.

A. Deque = [`'W','X','Z'`]  
B. Deque = [`'Y','W','X','Z'`]  
C. Front element = `'W'`, Rear element = `'Z'`  
D. Size = 3 after operations.

---

### [MCQ 5]
An array-based circular queue of capacity 5 uses indices `front` and `rear`.  
Initially `front = rear = 0`. After 4 enqueue and 2 dequeue operations, which condition indicates **fullness**?

A. `front == rear`  
B. `(rear + 1) % 5 == front`  
C. `rear == front - 1`  
D. `(front + rear) % 5 == 0`

---

### [MSQ 6]
Suppose Quick Sort uses **Hoare’s partition** with pivot = first element.  
For array `[9, 1, 8, 2, 7, 3, 6]`, which statements are TRUE after first partition?

A. All elements ≤ pivot are on its left.  
B. Pivot may not be at final sorted index.  
C. At least one comparison per element is guaranteed.  
D. Total swaps ≤ comparisons / 2.

---

### [MCQ 7]
Consider a recursive function:

```python
def fun(n):
    if n <= 1:
        return 1
    return n * fun(n - 2)
```

For `fun(6)`, how many frames exist **simultaneously** on the call stack at peak depth?

A. 3 
B. 4 
C. 5 
D. 6  

---

### [MSQ 8]
If we implement both stack and queue APIs using a deque object `D`, which calls are valid without modifying its invariants?

A. `D.addRear(x)` implements `push(x)`  
B. `D.removeRear()` implements `pop()`  
C. `D.addRear(x)` implements `enqueue(x)`  
D. `D.removeFront()` implements `dequeue()`

---

### [MCQ 9]
A hybrid sorting algorithm switches from Quick Sort to Insertion Sort for small subarrays.  
If threshold = 16 and average partition balance = 50–50, what is asymptotic time complexity?

A. O(n²)  
B. O(n log n)  
C. O(n √log n)  
D. O(log² n)

---

### [MSQ 10]
Select all statements that preserve **queue ADT invariants** in linked-list implementation.

A. Always maintain both `front` and `rear` pointers valid or `None`.  
B. On dequeue, update `front = front.next`; if empty → set `rear = None`.  
C. On enqueue, insert at front for efficiency.  
D. Ensure constant-time operations without full list traversal.