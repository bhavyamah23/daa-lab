<div align="center">

# MODY UNIVERSITY OF SCIENCE AND TECHNOLOGY

## School of Engineering and Technology

<br>

<img width="154" height="157" alt="Mody_University_logo" src="https://github.com/user-attachments/assets/11e32514-7869-4f2d-afc9-b45171b58488" />


<br>

# DESIGN ANALYSIS AND ALGORITHM LAB

### LAB RECORD

<br><br>

**Student Name:** Bhavya Maheshwari
**Enrollment Number:** 240029

<br>

**Faculty Name:** Dr. P. K. Bishnoi

<br><br>

**Mody University of Science and Technology**
**School of Engineering and Technology**
Lakshmangarh, Rajasthan

</div>

---

<div style="page-break-after: always;"></div>

# INDEX

# INDEX

<table style="width:100%; border-collapse:collapse;">
  <tr>
    <th style="width:10%;">S. No.</th>
    <th style="width:65%;">Program</th>
    <th style="width:25%;">Link</th>
  </tr>

  <tr>
    <td>1</td>
    <td>Addition of Two Numbers</td>
    <td><a href="#program-1-addition-of-two-numbers">Program 1</a></td>
  </tr>

  <tr>
    <td>2</td>
    <td>Largest of Three Numbers</td>
    <td><a href="#program-2-largest-of-three-numbers">Program 2</a></td>
  </tr>

  <tr>
    <td>3</td>
    <td>Factorial of a Number</td>
    <td><a href="#program-3-factorial-of-a-number">Program 3</a></td>
  </tr>

  <tr>
    <td>4</td>
    <td>Prime Number Check</td>
    <td><a href="#program-4-prime-number-check">Program 4</a></td>
  </tr>

  <tr>
    <td>5</td>
    <td>Fibonacci Series</td>
    <td><a href="#program-5-fibonacci-series">Program 5</a></td>
  </tr>
  <tr>
    <td>6</td>
    <td>Bubble Sort</td>
    <td><a href="#program-6-bubble-sort">Program 6</a></td>
  </tr>
  <tr>
    <td>7</td>
    <td>Merge Sort</td>
    <td><a href="#program-7-merge-sort">Program 7</a></td>
  </tr>
  <tr>
    <td>8</td>
    <td>Insertion Sort</td>
    <td><a href="#program-8-insertion-sort">Program 8</a></td>
  </tr>
  <tr>
    <td>9</td>
    <td>Selection Sort</td>
    <td><a href="#program-9-selection-sort">Program 9</a></td>
  </tr>
  <tr>
  <td>10</td>
    <td>Quick Sort</td>
    <td><a href="#program-10-quick-sort">Program 10</a></td>
  </tr>
  <tr>
    <td>11</td>
    <td>Linear Search</td>
    <td><a href="#program-11-linear-search">Program 11</a></td>
  </tr>
  <tr>
    <td>12</td>
    <td>Binary Search</td>
    <td><a href="#program-12-Binary-search">Program 12</a></td>
  </tr>
  <tr>
    <td>13</td>
    <td>Different Time Complexities, Execution Time and Memory Usage</td>
    <td><a href="#program-13-demonstration-of-different-time-complexities">Program 13</a></td>
  </tr>
</table>


---

<div style="page-break-after: always;"></div>

# Program 1: Addition of Two Numbers

## Aim

To write a Python program to find the sum of two numbers.

## Program

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

sum = a + b

print("Sum =", sum)
```

## Sample Output

```text
Enter first number: 10
Enter second number: 20
Sum = 30
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 2: Largest of Three Numbers

## Aim

To write a Python program to find the largest among three numbers.

## Program

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    largest = a
elif b >= a and b >= c:
    largest = b
else:
    largest = c

print("Largest number =", largest)
```

## Sample Output

```text
Enter first number: 10
Enter second number: 25
Enter third number: 15
Largest number = 25
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 3: Factorial of a Number

## Aim

To write a Python program to calculate the factorial of a given number.

## Program

```python
n = int(input("Enter a number: "))

fact = 1

for i in range(1, n + 1):
    fact = fact * i

print("Factorial =", fact)
```

## Sample Output

```text
Enter a number: 5
Factorial = 120
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 4: Prime Number Check

## Aim

To write a Python program to check whether a given number is prime or not.

## Program

```python
n = int(input("Enter a number: "))

prime = True

if n < 2:
    prime = False
else:
    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

if prime:
    print(n, "is a Prime Number")
else:
    print(n, "is not a Prime Number")
```

## Sample Output

```text
Enter a number: 7
7 is a Prime Number
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 5: Fibonacci Series

## Aim

To write a Python program to generate the Fibonacci series.

## Program

```python
n = int(input("Enter number of terms: "))

a = 0
b = 1

for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

## Sample Output

```text
Enter number of terms: 7
0 1 1 2 3 5 8
```

[Back to Index](#index)

---

<div style="page-break-after: always;"></div>

# Program 6: Bubble Sort

## Aim

To write a Python program to sort the elements of an array using Bubble Sort.

## Program

```python
import time
import tracemalloc
arr = [64, 34, 25, 12, 22, 11, 90]
tracemalloc.start()
start = time.perf_counter()
n = len(arr)
for i in range(n):
    for j in range(0, n-i-1):
        if arr[j] > arr[j+1]:
            arr[j], arr[j+1] = arr[j+1], arr[j]
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
print("Sorted Array:", arr)
print("Execution Time:", end-start, "seconds")
print("Memory Used:", peak, "bytes")
```

## Sample Output

```text
Sorted Array: [11, 12, 22, 25, 34, 64, 90]
Execution Time: 0.0019899999897461385 seconds
Memory Used: 880 bytes
```

[Back to Index](#index)

# Program 7: Merge Sort

## Aim

To write a Python program to sort the elements of an array using Merge Sort.

## Program

```python
import time
import tracemalloc
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        left = arr[:mid]
        right = arr[mid:]
        merge_sort(left)
        merge_sort(right)
        i = 0
        j = 0
        k = 0
        while i < len(left) and j < len(right):
            if left[i] < right[j]:
                arr[k] = left[i]
                i += 1
            else:
                arr[k] = right[j]
                j += 1
            k += 1
        while i < len(left):
            arr[k] = left[i]
            i += 1
            k += 1
        while j < len(right):
            arr[k] = right[j]
            j += 1
            k += 1
arr = [38, 27, 43, 3, 9, 82, 10]
tracemalloc.start()
start = time.perf_counter()
merge_sort(arr)
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
print("Sorted Array:", arr)
print("Execution Time:", end-start, "seconds")
print("Memory Used:", peak, "bytes")
```

## Sample Output

```text
Sorted Array: [3, 9, 10, 27, 38, 43, 82]
Execution Time: 0.012692500007688068 seconds
Memory Used: 936 bytes
```

[Back to Index](#index)

# Program 8: Insertion Sort

## Aim

To write a Python program to sort the elements of an array using Insertion Sort.

## Program

```python
import time
import tracemalloc
arr = [12, 11, 13, 5, 6, 8, 2]
tracemalloc.start()
start = time.perf_counter()
for i in range(1, len(arr)):
    key = arr[i]
    j = i - 1
    while j >= 0 and arr[j] > key:
        arr[j+1] = arr[j]
        j = j - 1
    arr[j+1] = key
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
print("Sorted Array:", arr)
print("Execution Time:", end-start, "seconds")
print("Memory Used:", peak, "bytes")
```

## Sample Output

```text
Sorted Array: [2, 5, 6, 8, 11, 12, 13]
Execution Time: 4.130000888835639e-05 seconds
Memory Used: 800 bytes
```

[Back to Index](#index)

# Program 9: Selection Sort

## Aim

To write a Python program to sort the elements of an array using Selection Sort.

## Program

```python
import time
import tracemalloc
arr = [64, 25, 12, 22, 11, 90, 34]
tracemalloc.start()
start = time.perf_counter()
n = len(arr)
for i in range(n):
    min_index = i
    for j in range(i+1, n):
        if arr[j] < arr[min_index]:
            min_index = j
    arr[i], arr[min_index] = arr[min_index], arr[i]
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
print("Sorted Array:", arr)
print("Execution Time:", end-start, "seconds")
print("Memory Used:", peak, "bytes")
```

## Sample Output

```text
Sorted Array: [11, 12, 22, 25, 34, 64, 90]
Execution Time: 8.510000770911574e-05 seconds
Memory Used: 880 bytes
```

[Back to Index](#index)

# Program 10: Quick Sort

## Aim

To write a Python program to sort the elements of an array using Quick Sort.

## Program

```python
import time
import tracemalloc
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr)//2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)
arr = [10, 7, 8, 9, 1, 5, 12]
tracemalloc.start()
start = time.perf_counter()
arr = quick_sort(arr)
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
print("Sorted Array:", arr)
print("Execution Time:", end-start, "seconds")
print("Memory Used:", peak, "bytes")
```

## Sample Output

```text
Sorted Array: [1, 5, 7, 8, 9, 10, 12]
Execution Time: 0.00010119999933522195 seconds
Memory Used: 1496 bytes
```

[Back to Index](#index)

# Program 11: Linear Search

## Aim

To write a Python program to search for an element in an array using Linear Search and analyze its execution time and memory usage.

## Program

```python
import time
import tracemalloc
n = int(input("Enter number of elements: "))
arr = []
for i in range(n):
    arr.append(int(input("Enter element: ")))
key = int(input("Enter element to search: "))
tracemalloc.start()
start = time.perf_counter()
found = -1
for i in range(n):
    if arr[i] == key:
        found = i
        break
end = time.perf_counter()
current, peak = tracemalloc.get_traced_memory()
tracemalloc.stop()
if found != -1:
    print("Element found at index:", found)
else:
    print("Element not found")
print("Execution Time =", end - start, "seconds")
print("Memory Used =", peak, "bytes")
```

## Sample Output

```text
Enter number of elements: 4
Enter element: 6
Enter element: 2
Enter element: 3
Enter element: 5
Enter element to search: 5
Element found at index: 3
Execution Time = 5.529999907594174e-05 seconds
Memory Used = 80 bytes
```

[Back to Index](#index)

# Program 12: Binary Search

## Aim

To write a Python program to implement Binary Search for finding a given element in a sorted array and calculate its execution time and memory used.

## Program

```python
import time
import sys
n = int(input("Enter number of elements: "))
arr = []
for i in range(n):
    arr.append(int(input("Enter element: ")))
# Sort the array
arr.sort()
key = int(input("Enter element to search: "))
# Start execution time
start = time.perf_counter()
low = 0
high = n - 1
found = -1
# Binary Search
while low <= high:
    mid = (low + high) // 2
    if arr[mid] == key:
        found = mid
        break
    elif arr[mid] < key:
        low = mid + 1
    else:
        high = mid - 1
# End execution time
end = time.perf_counter()
print("Sorted Array =", arr)
if found != -1:
    print("Element found at position:", found + 1)
else:
    print("Element not found")
print("Execution Time =", end - start, "seconds")
# Memory used by array
memory_used = sys.getsizeof(arr) + sum(sys.getsizeof(x) for x in arr)
print("Memory Used =", memory_used, "bytes")
```

## Sample Output

```text
Enter number of elements: 4
Enter element: 7
Enter element: 4
Enter element: 8
Enter element: 2
Enter element to search: 8
Sorted Array = [2, 4, 7, 8]
Element found at position: 4
Execution Time = 4.4000043999403715e-06 seconds
Memory Used = 200 bytes
```

[Back to Index](#index)

# Program 13: Demonstration of Different Time Complexities 

## Aim

To write a Python program to demonstrate different time complexities such as O(1), O(log n), O(√n), O(n), O(n log n), O(n²), O(n³), O(2ⁿ), and O(n!), and to calculate execution time and memory usage.

## Program

```python
# ============================================================
# QUESTION:
# Write a Python program to demonstrate different time
# complexities and calculate execution time and memory usage.
# ============================================================

import time
import tracemalloc
import math
from itertools import permutations


# ------------------------------------------------------------
# 1. O(1) - Constant Time
# ------------------------------------------------------------
print("\n========== O(1) - CONSTANT TIME ==========")

a = [10, 20, 30]

print("Array:", a)
print("First element:", a[0])


# ------------------------------------------------------------
# 2. O(log n) - Logarithmic Time
# ------------------------------------------------------------
print("\n========== O(log n) - LOGARITHMIC TIME ==========")

n = 16
original_n = n

while n > 1:
    n = n // 2

print("Original n:", original_n)
print("Value after repeated division:", n)


# ------------------------------------------------------------
# 3. O(sqrt(n)) - Square Root Time
# ------------------------------------------------------------
print("\n========== O(sqrt(n)) - SQUARE ROOT TIME ==========")

n = 25
i = 1

while i * i <= n:
    i += 1

print("n =", n)
print("Number of iterations:", i - 1)


# ------------------------------------------------------------
# 4. O(n) - Linear Time
# ------------------------------------------------------------
print("\n========== O(n) - LINEAR TIME ==========")

n = 5

for i in range(n):
    print("i =", i)


# ------------------------------------------------------------
# 5. O(n log n) - Linearithmic Time
# ------------------------------------------------------------
print("\n========== O(n log n) - LINEARITHMIC TIME ==========")

n = 8

for i in range(n):
    j = i

    while j > 1:
        j = j // 2

    print("i =", i, "final j =", j)


# ------------------------------------------------------------
# 6. O(n^2) - Quadratic Time
# ------------------------------------------------------------
print("\n========== O(n^2) - QUADRATIC TIME ==========")

n = 3

for i in range(n):
    for j in range(n):
        print("(", i, ",", j, ")")


# ------------------------------------------------------------
# 7. O(n^3) - Cubic Time
# ------------------------------------------------------------
print("\n========== O(n^3) - CUBIC TIME ==========")

n = 2

for i in range(n):
    for j in range(n):
        for k in range(n):
            print("(", i, ",", j, ",", k, ")")


# ------------------------------------------------------------
# 8. O(2^n) - Exponential Time
# ------------------------------------------------------------
print("\n========== O(2^n) - EXPONENTIAL TIME ==========")

def fun_exponential(n):

    if n == 0:
        return

    print(n)

    fun_exponential(n - 1)
    fun_exponential(n - 1)


print("Output for n = 3:")
fun_exponential(3)


# ------------------------------------------------------------
# 9. O(n!) - Factorial Time
# ------------------------------------------------------------
print("\n========== O(n!) - FACTORIAL TIME ==========")

n = 3

for p in permutations(range(n)):
    print(p)


# ------------------------------------------------------------
# 10. EXECUTION TIME
# ------------------------------------------------------------
print("\n========== EXECUTION TIME ==========")

start = time.time()

for i in range(1000000):
    pass

end = time.time()

print("Execution Time:", end - start, "seconds")


# ------------------------------------------------------------
# 11. MEMORY USED
# ------------------------------------------------------------
print("\n========== MEMORY USED ==========")

tracemalloc.start()

a = [i for i in range(100000)]

current, peak = tracemalloc.get_traced_memory()

print("Current Memory:", current, "bytes")
print("Peak Memory:", peak, "bytes")

tracemalloc.stop()


# ------------------------------------------------------------
# 12. GRAPH PLOT - COMPARISON OF TIME COMPLEXITIES
# ------------------------------------------------------------
print("\n========== GRAPH ==========")

n_values = range(1, 11)

O_1 = [1 for n in n_values]
O_log_n = [math.log2(n) for n in n_values]
O_sqrt_n = [n ** 0.5 for n in n_values]
O_n = [n for n in n_values]
O_n_log_n = [n * math.log2(n) for n in n_values]
O_n2 = [n ** 2 for n in n_values]
O_n3 = [n ** 3 for n in n_values]
O_2n = [2 ** n for n in n_values]

import matplotlib.pyplot as plt

plt.figure(figsize=(10, 6))

plt.plot(n_values, O_1, marker='o', label='O(1)')
plt.plot(n_values, O_log_n, marker='o', label='O(log n)')
plt.plot(n_values, O_sqrt_n, marker='o', label='O(sqrt(n))')
plt.plot(n_values, O_n, marker='o', label='O(n)')
plt.plot(n_values, O_n_log_n, marker='o', label='O(n log n)')
plt.plot(n_values, O_n2, marker='o', label='O(n^2)')
plt.plot(n_values, O_n3, marker='o', label='O(n^3)')
plt.plot(n_values, O_2n, marker='o', label='O(2^n)')
plt.xlabel("Input Size (n)")
plt.ylabel("Number of Operations / Growth")
plt.title("Comparison of Time Complexities")
plt.legend()
plt.grid(True)
plt.show()
# ------------------------------------------------------------
# END
# ------------------------------------------------------------
print("\n==============================================")
print("       ALL COMPLEXITIES EXECUTED SUCCESSFULLY")
print("==============================================")
```

## Sample Output

```text
========== O(1) - CONSTANT TIME ==========
Array: [10, 20, 30]
First element: 10

========== O(log n) - LOGARITHMIC TIME ==========
Original n: 16
Value after repeated division: 1

========== O(sqrt(n)) - SQUARE ROOT TIME ==========
n = 25
Number of iterations: 5

========== O(n) - LINEAR TIME ==========
i = 0
i = 1
i = 2
i = 3
i = 4

========== O(n log n) - LINEARITHMIC TIME ==========
i = 0 final j = 0
i = 1 final j = 1
i = 2 final j = 1
i = 3 final j = 1
i = 4 final j = 1
i = 5 final j = 1
i = 6 final j = 1
i = 7 final j = 1

========== O(n^2) - QUADRATIC TIME ==========
( 0 , 0 )
( 0 , 1 )
( 0 , 2 )
( 1 , 0 )
( 1 , 1 )
( 1 , 2 )
( 2 , 0 )
( 2 , 1 )
( 2 , 2 )

========== O(n^3) - CUBIC TIME ==========
( 0 , 0 , 0 )
( 0 , 0 , 1 )
( 0 , 1 , 0 )
( 0 , 1 , 1 )
( 1 , 0 , 0 )
( 1 , 0 , 1 )
( 1 , 1 , 0 )
( 1 , 1 , 1 )

========== O(2^n) - EXPONENTIAL TIME ==========
Output for n = 3:
3
2
1
1
2
1
1

========== O(n!) - FACTORIAL TIME ==========
(0, 1, 2)
(0, 2, 1)
(1, 0, 2)
(1, 2, 0)
(2, 0, 1)
(2, 1, 0)

========== EXECUTION TIME ==========
Execution Time: 0.019642353057861328 seconds

========== MEMORY USED ==========
Current Memory: 3993016 bytes
Peak Memory: 3993048 bytes

==============================================
       ALL COMPLEXITIES EXECUTED SUCCESSFULLY
==============================================

```
<img width="927" height="567" alt="1" src="https://github.com/user-attachments/assets/72161281-a154-4f7a-9200-7a7a899b559b" />

[Back to Index](#index)
