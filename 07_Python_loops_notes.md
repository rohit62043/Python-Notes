# Python Loops – Detailed Notes

## 1. Introduction to Loops
Loops in Python are used to repeatedly execute a block of code until a specified condition is met.

### Types of Loops in Python
- **For Loop** – Iterates over a sequence (list, tuple, string, range, etc.).
- **While Loop** – Repeats execution as long as a given condition is `True`.
- **Loop Control Statements** – `break`, `continue`, and `pass`.
- **Nested Loops** – Loop inside another loop.

---

## 2. **For Loop**

### Syntax
```python
for variable in sequence:
    # code block
```

### Iterating with `range()`
- **Syntax:** `range(start, stop, step)`
  - **start**: starting value (default = 0)
  - **stop**: ending value (exclusive)
  - **step**: increment value (default = 1)

#### Examples:
```python
for i in range(5):
    print(i)  # 0,1,2,3,4

for i in range(1, 6):
    print(i)  # 1,2,3,4,5

for i in range(1, 10, 2):
    print(i)  # 1,3,5,7,9

for i in range(10, 0, -1):
    print(i)  # 10,9,8,...,1
```

### Iterating Over Strings
```python
text = "Krish Nayak"
for ch in text:
    print(ch)  # Prints each character
```

---

## 3. **While Loop**

### Definition
Executes a block of code **while** a condition is `True`.

### Syntax
```python
while condition:
    # code block
```

#### Example:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

---

## 4. **Loop Control Statements**

### 4.1 `break`
- Exits the loop prematurely when a condition is met.
```python
for i in range(10):
    if i == 5:
        break
    print(i)  # 0,1,2,3,4
```

### 4.2 `continue`
- Skips the current iteration and moves to the next one.
```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # Prints odd numbers: 1,3,5,7,9
```

### 4.3 `pass`
- Does nothing; acts as a placeholder.
```python
for i in range(5):
    if i == 3:
        pass  # placeholder
    print(i)
```

---

## 5. **Nested Loops**
A loop inside another loop.
```python
for i in range(3):
    for j in range(2):
        print(f"i = {i}, j = {j}")
```

---

## 6. **Practical Examples**

### Example 1: Sum of First `n` Natural Numbers
**Using While Loop:**
```python
n = 10
sum_ = 0
count = 1
while count <= n:
    sum_ += count
    count += 1
print("Sum:", sum_)  # 55
```

**Using For Loop:**
```python
n = 10
sum_ = 0
for i in range(1, n+1):
    sum_ += i
print("Sum:", sum_)  # 55
```

### Example 2: Prime Numbers Between 1 and 100
```python
for num in range(1, 101):
    if num > 1:
        for i in range(2, num):
            if num % i == 0:
                break
        else:
            print(num)
```

---

## 7. **Conclusion**
- Loops are essential for repetitive tasks.
- **For loops** are best for iterating over sequences.
- **While loops** are useful when the number of iterations is not known in advance.
- **Break**, **continue**, and **pass** provide fine control over loop execution.
- Nested loops allow working with multiple sequences.

> Mastering loops is key to solving problems efficiently in Python.

