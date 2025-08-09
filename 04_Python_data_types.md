# Python Data Types - Detailed Notes

## 1. Introduction to Data Types

**Definition:** Data types are classifications of data that tell the compiler or interpreter how the programmer intends to use the data.

**Purpose:**

- Determine the type of operations that can be performed.
- Define the values data can hold.
- Specify the amount of memory required to store the data.

---

## 2. Importance of Data Types in Programming

- **Efficient Data Storage:** Ensures data is stored optimally in memory.
- **Correct Operations:** Prevents invalid operations on incompatible data types.
- **Error Prevention:** Helps reduce bugs by enforcing type rules.
- **Memory Management:** Allocates appropriate memory based on the data type.

---

## 3. Basic Data Types in Python

### 3.1 Integer (`int`)

- Whole numbers without a decimal point.
- Example:

```python
age = 35
print(type(age))  # <class 'int'>
```

### 3.2 Floating Point Numbers (`float`)

- Numbers with decimal points.
- Example:

```python
height = 5.11
print(height)       # 5.11
print(type(height)) # <class 'float'>
```

### 3.3 Strings (`str`)

- Sequence of characters enclosed in single or double quotes.
- Example:

```python
name = "Krish"
print(name)        # Krish
print(type(name))  # <class 'str'>
```

### 3.4 Boolean (`bool`)

- Represents truth values: `True` or `False`.
- Example 1:

```python
is_true = True
print(type(is_true))  # <class 'bool'>
```

- Example 2:

```python
a = 10
b = 10
print(a == b)         # True
print(type(a == b))   # <class 'bool'>
```

---

## 4. Type Conversion (Typecasting)

- **Definition:** Converting one data type into another.
- Example:

```python
result = "Hello"
# Attempt to add integer to string → Error
# result + 5  # TypeError: can only concatenate str (not "int") to str

# Correct way:
result = result + str(5)
print(result)  # Hello5
```

---

## 5. Common Errors with Data Types

- **String and Integer Concatenation Error:** Cannot directly concatenate a string with an integer.
- **Solution:** Convert integer to string using `str()`.

---

## 6. String Methods Overview

Strings in Python have many built-in methods, for example:

- `.isalpha()` - Checks if all characters are alphabetic.
- `.isdigit()` - Checks if all characters are digits.
- `.lower()` / `.upper()` - Changes case.
- `.strip()` - Removes whitespace.
- `.replace()` - Replaces substring.

**Example:**

```python
text = " Hello World "
print(text.strip())  # "Hello World"
```

---

## 7. Summary

- Data types classify and define how data can be stored and manipulated.
- Basic Python data types: `int`, `float`, `str`, `bool`.
- Typecasting allows converting between compatible data types.
- Understanding data types helps in error prevention, efficient memory use, and correct program logic.

---

**Next Step:** In upcoming lessons, we will explore advanced data types like `list`, `tuple`, `set`, and `dict`, along with their operations.

