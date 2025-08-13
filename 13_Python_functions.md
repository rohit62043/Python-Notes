# **Python Functions - Comprehensive Notes**

## **1. Introduction to Functions**

A **function** is a reusable block of code designed to perform a specific task. Functions help in:

- Organizing code logically
- Avoiding redundancy by reusing code
- Improving readability and maintainability

**Definition:**

> A function is a named sequence of statements that performs a computation or action.

---

## **2. Syntax of a Function**

```python
def function_name(parameters):
    """Docstring explaining the purpose of the function"""
    # Function body
    return value  # Optional
```

**Components:**

- `def`: Keyword to define a function
- **Function Name**: Should follow Python naming conventions
- **Parameters**: Input values (optional)
- **Docstring**: Explains purpose and usage
- **Function Body**: Code block to execute
- **Return Statement**: Sends value(s) back (optional)

---

## **3. Why Use Functions?**

- Avoid code repetition
- Make code easier to maintain
- Facilitate testing and debugging
- Improve collaboration in projects

**Example:**

```python
def even_or_odd(num):
    if num % 2 == 0:
        print("Even")
    else:
        print("Odd")
```

---

## **4. Parameters in Functions**

### Single Parameter

```python
def greet(name):
    print(f"Hello {name}, Welcome!")
```

### Multiple Parameters

```python
def add(a, b):
    return a + b
```

---

## **5. Default Parameters**

```python
def greet(name="Guest"):
    print(f"Hello {name}, Welcome!")

greet()       # Hello Guest, Welcome!
greet("Rohit")
```

---

## **6. Variable-Length Arguments**

### Positional (`*args`)

```python
def print_numbers(*args):
    for num in args:
        print(num)
```

### Keyword (`**kwargs`)

```python
def print_details(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

### Both Together

```python
def show_info(*args, **kwargs):
    print(args)
    print(kwargs)
```

---

## **7. Return Statement**

```python
def multiply(a, b):
    return a * b
```

Multiple returns:

```python
def values(a, b):
    return a, b, a + b
```

---

## **8. Best Practices**

- Use descriptive names
- Keep functions focused on a single task
- Write clear docstrings
- Use `*args`/`**kwargs` for flexibility
- Avoid unintended side effects

---

## **9. Summary Table**

| Feature          | Syntax              | Description                   |
| ---------------- | ------------------- | ----------------------------- |
| Define           | `def name(params):` | Create a new function         |
| Single Param     | `def f(x):`         | Takes one argument            |
| Multiple Params  | `def f(a, b):`      | Multiple arguments            |
| Default Param    | `def f(x=10):`      | Uses default if missing       |
| Positional Args  | `*args`             | Variable positional arguments |
| Keyword Args     | `**kwargs`          | Variable keyword arguments    |
| Return           | `return val`        | Sends value back              |
| Multiple Returns | `return a, b`       | Returns tuple                 |

---

## **Conclusion**

Functions are the backbone of clean and maintainable Python programs. They:

- Break down complex problems into smaller, manageable tasks
- Enable code reuse instead of rewriting
- Improve readability and collaboration

By mastering parameters, return values, and best practices, you can design functions that are both **efficient** and **easy to maintain**.

**Key Takeaway:**

> Mastering functions is one of the most valuable skills in Python. Once comfortable, explore **lambda functions, decorators, and higher-order functions** to write more advanced and expressive code.

