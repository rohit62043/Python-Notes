# Python `filter()` Function — Detailed Notes

## 1. Introduction

The `` function in Python constructs an iterator from elements of an iterable **for which a function returns **``. It is commonly used to filter out items from lists, tuples, or any iterable based on a given condition.

**Key Points:**

- Takes **two arguments**: a function and an iterable.
- The function should return a boolean value (`True` or `False`).
- Only elements for which the function returns `True` are included in the result.
- Returns a **filter object** (iterator) — often converted to a `list` or `tuple` for display.

---

## 2. Basic Syntax

```python
filter(function, iterable)
```

- **function** → A function that tests each element.
- **iterable** → The sequence (list, tuple, set, etc.) to filter.

---

## 3. Example 1 — Filtering Even Numbers

```python
def is_even(num):
    return num % 2 == 0

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
result = list(filter(is_even, numbers))
print(result)  # [2, 4, 6, 8, 10, 12]
```

**Explanation:**

- Function `is_even` checks if a number is divisible by 2.
- `filter()` applies `is_even` to each element.
- Only numbers returning `True` are kept.

---

## 4. Example 2 — Using `filter()` with Lambda

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
result = list(filter(lambda x: x > 5, numbers))
print(result)  # [6, 7, 8, 9]
```

**Explanation:**

- Lambda function `lambda x: x > 5` checks if numbers are greater than 5.
- Returns only numbers greater than 5.

---

## 5. Example 3 — Multiple Conditions in `filter()`

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
result = list(filter(lambda x: x > 5 and x % 2 == 0, numbers))
print(result)  # [6, 8]
```

**Explanation:**

- Checks **two conditions**:
  1. Number must be greater than 5.
  2. Number must be even.
- Only numbers satisfying both conditions are included.

---

## 6. Example 4 — Filtering Data from a Dictionary

```python
people = [
    {"name": "Alice", "age": 32},
    {"name": "Bob", "age": 25},
    {"name": "Charlie", "age": 33},
    {"name": "David", "age": 24}
]

def age_greater_than_25(person):
    return person['age'] > 25

result = list(filter(age_greater_than_25, people))
print(result)
# [{'name': 'Alice', 'age': 32}, {'name': 'Charlie', 'age': 33}]
```

**Explanation:**

- The function checks if a person's age is greater than 25.
- `filter()` returns only matching dictionaries.

---

## 7. Practical Use Cases

- **Data Cleaning:** Remove unwanted elements.
- **Filtering Objects:** Select records matching a condition.
- **Optimizing Loops:** Avoid manual iteration and `if` statements.

---

## 8. Conclusion

- `filter()` is a **powerful tool** for extracting data based on conditions.
- Works well with **named functions** and **lambda expressions**.
- Can handle **multiple conditions** and **complex data structures**.
- Improves **code readability** and reduces the need for manual filtering loops.

**Mastering **`` allows writing **concise**, **efficient**, and **clean** Python code for processing and manipulating collections.

