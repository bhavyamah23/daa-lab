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

