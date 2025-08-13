# Python Lists — Detailed Structured Notes

## 1. Definition & Properties

- **List**: A collection of items (elements) enclosed in square brackets `[]`.
- **Mutable**: Elements can be changed after creation.
- Can store **mixed data types** (integers, floats, strings, etc.).
- Indexed starting from **0** (positive indexing) or from **-1** (negative indexing).
- Lists are **ordered** (maintain insertion order).

---

## 2. Creating Lists

```python
# Empty list
my_list = []

# List with elements
fruits = ["apple", "banana", "cherry"]

# Mixed data types
mixed = [1, "hello", 3.14, True]
```

---

## 3. Accessing Elements

### Positive Indexing

```python
fruits[0]   # 'apple'
fruits[1]   # 'banana'
```

### Negative Indexing

```python
fruits[-1]  # 'cherry'
fruits[-2]  # 'banana'
```

---

## 4. Modifying Elements

```python
fruits[1] = "blueberry"  # Replace 'banana' with 'blueberry'
```

---

## 5. Common List Methods

### Adding Elements

```python
# Append to the end
fruits.append("orange")

# Insert at a position
fruits.insert(1, "kiwi")
```

### Removing Elements

```python
# Remove by value
fruits.remove("apple")

# Remove by index & return removed element
removed_item = fruits.pop(2)

# Clear all elements
fruits.clear()
```

### Searching & Counting

```python
index = fruits.index("banana")  # First occurrence
count = fruits.count("banana")  # Number of occurrences
```

### Sorting & Reversing

```python
fruits.sort()     # Sort ascending
fruits.sort(reverse=True)  # Sort descending
fruits.reverse()  # Reverse order
```

---

## 6. Slicing

### Syntax:

```python
list[start:end:step]
```

- `start`: Starting index (inclusive)
- `end`: Ending index (exclusive)
- `step`: Step size (default is 1)

### Examples:

```python
numbers = [0, 1, 2, 3, 4, 5]

numbers[1:4]    # [1, 2, 3]
numbers[:3]     # [0, 1, 2]
numbers[2:]     # [2, 3, 4, 5]
numbers[::2]    # [0, 2, 4]
numbers[::-1]   # [5, 4, 3, 2, 1, 0]  (reverse)
```

---

## 7. Iterating Over Lists

### Using `for` loop:

```python
for fruit in fruits:
    print(fruit)
```

### Using `enumerate()` for index & value:

```python
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

---

## 8. List Comprehensions

- Concise way to create lists.
- Syntax:

```python
[expression for item in iterable if condition]
```

### Examples:

```python
# Squares of numbers
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]

# Even numbers
evens = [x for x in range(10) if x % 2 == 0]  # [0, 2, 4, 6, 8]

# Convert strings to uppercase
fruits_upper = [fruit.upper() for fruit in fruits]
```

---

## 9. Summary Table of Methods

| Method      | Description                      |
| ----------- | -------------------------------- |
| `append()`  | Add item at the end              |
| `insert()`  | Add item at specific position    |
| `remove()`  | Remove first occurrence of value |
| `pop()`     | Remove and return item by index  |
| `clear()`   | Remove all elements              |
| `index()`   | Return first occurrence index    |
| `count()`   | Count occurrences of value       |
| `sort()`    | Sort list                        |
| `reverse()` | Reverse list order               |

