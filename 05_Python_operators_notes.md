# Python Operators – Detailed Notes

## 1. Introduction to Operators

Operators in Python are special symbols or keywords that perform operations on variables and values. They can be used for arithmetic, comparison, and logical computations.

**Types covered in this video:**

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators

---

## 2. Arithmetic Operators

Arithmetic operators are used for mathematical calculations.

| Operator | Description         | Example (`a=10, b=5`) | Output   |
| -------- | ------------------- | --------------------- | -------- |
| `+`      | Addition            | `a + b`               | `15`     |
| `-`      | Subtraction         | `a - b`               | `5`      |
| `*`      | Multiplication      | `a * b`               | `50`     |
| `/`      | Division            | `a / b`               | `2.0`    |
| `//`     | Floor Division      | `21 // 5`             | `4`      |
| `%`      | Modulus (Remainder) | `10 % 5`              | `0`      |
| `**`     | Exponentiation      | `a ** b`              | `100000` |

### Floor Division (`//`) vs Division (`/`)

- `/` gives a floating-point result.
- `//` removes the decimal part and returns the largest integer less than or equal to the result.

Example:

```python
21 / 5   # Output: 4.2
21 // 5  # Output: 4
```

---

## 3. Comparison Operators

Comparison operators compare two values and return a boolean result (`True`/`False`).

| Operator | Description              | Example (`a=10, b=15`) | Output  |
| -------- | ------------------------ | ---------------------- | ------- |
| `==`     | Equal to                 | `a == b`               | `False` |
| `!=`     | Not equal to             | `a != b`               | `True`  |
| `>`      | Greater than             | `a > b`                | `False` |
| `<`      | Less than                | `a < b`                | `True`  |
| `>=`     | Greater than or equal to | `a >= b`               | `False` |
| `<=`     | Less than or equal to    | `a <= b`               | `True`  |

**Case Sensitivity in String Comparisons:**

```python
"Krish" == "krish"  # Output: False
```

Comparisons are case-sensitive.

---

## 4. Logical Operators

Logical operators are used to combine conditional statements.

| Operator | Description                               | Example (`x=True, y=False`) | Output  |
| -------- | ----------------------------------------- | --------------------------- | ------- |
| `and`    | True if both conditions are True          | `x and y`                   | `False` |
| `or`     | True if at least one condition is True    | `x or y`                    | `True`  |
| `not`    | Returns the opposite of the boolean value | `not x`                     | `False` |

**Truth Table:**

- `` → True only if *both* conditions are True.
- `` → False only if *both* conditions are False.
- `` → Inverts the boolean value.

Example:

```python
x = True
y = False

print(x and y)  # False
print(x or y)   # True
print(not x)    # False
```

---

## 5. Mini Calculator Example

Example program using arithmetic operators:

```python
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulus:", a % b)
print("Exponentiation:", a ** b)
```

---

## Summary

- **Arithmetic Operators**: Perform basic math (`+ - * / // % **`).
- **Comparison Operators**: Compare values (`== != > < >= <=`).
- **Logical Operators**: Combine conditions (`and or not`).
- Python comparisons are **case-sensitive**.
- Floor division `//` removes the decimal part.
- Logical operators return boolean values based on conditions.

