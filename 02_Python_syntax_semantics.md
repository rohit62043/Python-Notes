# Python Programming: Syntax and Semantics

## 1. Introduction
This lecture covers the basics of **syntax** and **semantics** in Python, including:
- Single-line and multi-line comments
- Definitions of syntax and semantics
- Basic syntax rules
- Common syntax errors and how to avoid them
- Practical code examples

---

## 2. Definitions

### 2.1 Syntax
> Syntax refers to the set of rules that define the combination of symbols considered correctly structured programs in a language.

**Simplified:** It is the correct arrangement of words and symbols in the code.

Example:
```python
print("Hello")  # Correct syntax
print(Hello)    # Syntax error
```

### 2.2 Semantics
> Semantics refers to the meaning or interpretation of the symbols, characters, and commands in a language.

**Simplified:** It’s about what the code is supposed to do when it runs.

Example:
```python
# Syntax is correct, but semantics are wrong
print(10 / 0)  # Runtime error due to division by zero
```

---

## 3. Comments in Python

### 3.1 Single-line Comments
- Start with `#` or `##`.
- Used for brief explanations.
```python
# This is a single-line comment
print("Hello World")
```

### 3.2 Multi-line Comments
- Use triple quotes `'''` or `"""`.
- Typically used in `.py` files (not effective in Jupyter notebooks for commenting purposes).
```python
'''
This is a multi-line comment.
It spans multiple lines.
'''
```

---

## 4. Basic Syntax Rules in Python

### 4.1 Case Sensitivity
Python is **case-sensitive**.
```python
name = "Krish"
Name = "Nick"
print(name)  # Krish
print(Name)  # Nick
```

### 4.2 Indentation
- Python uses **indentation** to define code blocks.
- Typically **4 spaces** or **1 tab**.
```python
age = 32
if age > 30:
    print("Age is greater than 30")
```

### 4.3 Line Continuation
- Use a backslash `\` to continue a statement on the next line.
```python
total = 1 + 2 + 3 + 4 + 5 + 6 + \
        7 + 8 + 9
```

### 4.4 Multiple Statements in One Line
- Separate statements with a semicolon `;`.
```python
x = 5; y = 10; z = x + y
print(z)  # 15
```

---

## 5. Understanding Semantics in Python

### 5.1 Variable Assignment
- Python infers the type at runtime (**dynamic typing**).
```python
age = 32            # int
name = "Krish"      # str
print(type(age))    # <class 'int'>
print(type(name))   # <class 'str'>
```

### 5.2 Type Inference Example
```python
variable = 10
print(type(variable))  # int

variable = "Chris"
print(type(variable))  # str
```

---

## 6. Common Syntax Errors

### 6.1 Indentation Error
```python
age = 32
if age > 30:
print(age)  # ❌ IndentationError
```

### 6.2 Name Error
```python
a = b  # ❌ NameError: name 'b' is not defined
```

---

## 7. Indentation Example with Nested Blocks
```python
if True:
    print("Correct indentation")
    if False:
        print("Will not print")
    print("This will print")
print("Outside if block")
```
**Output:**
```
Correct indentation
This will print
Outside if block
```

---

## 8. Summary
In this session, we covered:
- **Single-line and multi-line comments**
- **Definition of syntax and semantics**
- **Basic syntax rules** (case sensitivity, indentation, line continuation, multiple statements)
- **Variable assignment and type inference**
- **Common syntax errors** and how to avoid them

**Next Topic:** Variables, Data Types, and Operators in Python.

