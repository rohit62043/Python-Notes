# Python Tuples - Detailed Structured Notes

## 1. Introduction to Tuples
- **Definition**: Tuples are **ordered collections of items** that are **immutable** (cannot be changed after creation).
- **Similarity with Lists**: Like lists, tuples can store elements of any data type and support indexing/slicing.
- **Difference from Lists**: Lists are mutable, tuples are immutable.

---

## 2. Creating Tuples
### 2.1 Empty Tuple
```python
empty_tuple = ()
print(empty_tuple)          # ()
print(type(empty_tuple))    # <class 'tuple'>
```

### 2.2 Using `tuple()` Constructor
```python
empty_tuple = tuple()
```

### 2.3 Tuple with Elements
```python
my_tuple = (1, 2, 3)
```

### 2.4 Converting from List to Tuple
```python
numbers = tuple([1, 2, 3, 4, 5, 6])
```

### 2.5 Converting Tuple to List
```python
list_numbers = list((1, 2, 3, 4, 5, 6))
```

### 2.6 Mixed Data Type Tuple
```python
mixed_tuple = (1, "Hello", 3.14, True)
```

---

## 3. Accessing Tuple Elements
### 3.1 Indexing
```python
numbers = (1, 2, 3, 4, 5, 6)
print(numbers[0])   # First element
print(numbers[-1])  # Last element
```

### 3.2 Slicing
```python
print(numbers[0:4])       # Elements from index 0 to 3
print(numbers[::-1])      # Reverse tuple
```

---

## 4. Tuple Operations
### 4.1 Concatenation
```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
result = tuple1 + tuple2
```

### 4.2 Repetition
```python
mixed_tuple = (1, "Hello", 3.14, True)
print(mixed_tuple * 3)
```

---

## 5. Immutability of Tuples
- **Mutable List Example**
```python
lst = [1, 2, 3]
lst[0] = "Krish"  # Works
```
- **Immutable Tuple Example**
```python
tup = (1, 2, 3)
tup[0] = "Krish"  # Error: 'tuple' object does not support item assignment
```
- **Workaround**: Convert tuple → list → modify → convert back to tuple.

---

## 6. Tuple Methods
Only **two** common methods:
```python
numbers = (1, 2, 3, 4, 5, 6)

# Count occurrences
print(numbers.count(1))   # 1

# Find index of first occurrence
print(numbers.index(3))   # 2
```

---

## 7. Packing and Unpacking Tuples
### 7.1 Packing
```python
packed_tuple = (1, "Hello", 3.14)
```

### 7.2 Unpacking
```python
a, b, c = packed_tuple
print(a, b, c)
```

### 7.3 Unpacking with `*`
```python
numbers = (1, 2, 3, 4, 5, 6)
first, *middle, last = numbers
print(first)   # 1
print(middle)  # [2, 3, 4, 5]
print(last)    # 6
```

---

## 8. Nested Tuples
### 8.1 Tuple inside a Tuple
```python
nested_tuple = ((1, 2, 3), ("a", "b", "c"), (True, False))
```

### 8.2 Accessing Nested Elements
```python
print(nested_tuple[0])       # (1, 2, 3)
print(nested_tuple[1][2])    # 'c'
```

### 8.3 Iterating over Nested Tuples
```python
for sub_tuple in nested_tuple:
    for item in sub_tuple:
        print(item, end=" ")
```

---

## 9. Key Points & Conclusion
- Tuples are **immutable ordered collections**.
- Useful when data should **not change**.
- Commonly used in:
  - Function arguments & return values
  - Dictionary keys
  - Data structures requiring immutability
- Understanding tuples improves **efficiency** & **readability** of Python code.

