# Python – Lambda Functions

## 1. Introduction
- **Lambda Functions**: Small, anonymous functions defined using the `lambda` keyword.
- **Anonymous Function**: A function without a name.
- **Key Properties**:
  - Any number of arguments
  - Only one expression (single logic)
  - Commonly used for short operations or as arguments to higher-order functions.

---

## 2. Syntax
```python
lambda arguments: expression
```
- **arguments** → Inputs to the function.
- **expression** → Single logic or operation.

---

## 3. Example 1 – Basic Addition
**Normal Function:**
```python
def add(a, b):
    return a + b
add(2, 3)  # Output: 5
```
**Lambda Function:**
```python
addition = lambda a, b: a + b
addition(5, 6)  # Output: 11
```

---

## 4. Example 2 – Check Even Number
**Normal Function:**
```python
def is_even(num):
    return num % 2 == 0
is_even(24)  # Output: True
```
**Lambda Function:**
```python
even1 = lambda num: num % 2 == 0
even1(12)  # Output: True
```

---

## 5. Example 3 – Multiple Parameters
**Normal Function:**
```python
def addition(x, y, z):
    return x + y + z
addition(12, 13, 14)  # Output: 39
```
**Lambda Function:**
```python
addition1 = lambda x, y, z: x + y + z
addition1(12, 13, 14)  # Output: 39
```

---

## 6. When to Use Lambda Functions
- For **short, simple functions**.
- When passing a function as an argument (e.g., `map`, `filter`, `sorted`).
- When avoiding writing full `def` blocks for one-line logic.

---

## 7. Map Function with Lambda
**Goal**: Square each number in a list.

**Using Normal Function:**
```python
def square(num):
    return num ** 2
```
**Using Map + Lambda:**
```python
numbers = [1, 2, 3, 4, 5, 6]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25, 36]
```

---

## 8. Key Points
- **Lambda** → Anonymous function (single expression).
- **Map** → Applies a function to all items in an iterable.
- **Lazy Evaluation** → Map returns an iterator, so conversion to list may be required.

