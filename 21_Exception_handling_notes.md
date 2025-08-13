# Python Exception Handling - Detailed Notes

## 1. **Definition of Exception Handling**
Exception handling in Python allows you to manage errors gracefully and take corrective actions without stopping the execution of the program.

---

## 2. **Difference Between Errors and Exceptions**
- **Error:** A problem in the program that may be caused by syntax issues or other problems preventing execution.
- **Exception:** An event that disrupts the normal flow of a program during execution.

**Common Exceptions:**
- `ZeroDivisionError`
- `FileNotFoundError`
- `ValueError`
- `TypeError`
- `NameError`

---

## 3. **Basic Exception Handling Syntax**
```python
try:
    # Code that may raise an exception
except SomeException:
    # Handle the exception
```
- `try`: Contains code where exceptions may occur.
- `except`: Catches and handles exceptions.

---

## 4. **Handling Specific Exceptions**
You can handle specific exceptions to give user-friendly messages.
```python
try:
    a = b
except NameError:
    print("The variable has not been assigned")
```

---

## 5. **Catching the Exception Object**
You can capture the exception object and display its message.
```python
try:
    a = b
except NameError as e:
    print(e)  # Outputs: name 'b' is not defined
```

---

## 6. **Multiple Exception Handling**
You can handle different exceptions with multiple `except` blocks.
```python
try:
    result = 1 / 0
except ZeroDivisionError as e:
    print(e)
    print("Please enter a denominator greater than zero")
```

---

## 7. **Base Exception Class**
- All exceptions are derived from the base `Exception` class.
- Use `Exception` to catch any type of exception.
```python
try:
    a = b
except Exception as e:
    print(e)
```
> **Note:** Always place `Exception` at the end of multiple exception blocks.

---

## 8. **Example: Handling Multiple Exceptions**
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("Not a valid number")
except ZeroDivisionError:
    print("Enter a denominator greater than zero")
except Exception as e:
    print(e)
```

---

## 9. **Else Block in Exception Handling**
- Runs only if no exception occurs.
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("Not a valid number")
except ZeroDivisionError:
    print("Enter a denominator greater than zero")
else:
    print(f"Result is {result}")
```

---

## 10. **Finally Block**
- Runs regardless of whether an exception occurs.
- Commonly used for cleanup operations (e.g., closing files or database connections).
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except Exception as e:
    print(e)
finally:
    print("Execution complete")
```

---

## 11. **Real-World Example with Files**
```python
try:
    file = open("example1.txt", "r")
    content = file.read()
    print(content)
except FileNotFoundError:
    print("The file does not exist")
finally:
    if 'file' in locals() and not file.closed:
        file.close()
        print("File closed")
```

---

## 12. **Best Practices**
- Use specific exceptions before generic ones.
- Always close resources using `finally` or `with` statement.
- Provide meaningful error messages for end-users.
- Avoid using bare `except:` without specifying the exception.

---

## 13. **Summary Table**
| Block      | Purpose |
|------------|---------|
| `try`      | Code that may raise an exception |
| `except`   | Handle the exception |
| `else`     | Executes if no exception occurs |
| `finally`  | Executes regardless of exceptions |

---

**Key Takeaway:** Exception handling improves program reliability, user experience, and prevents abrupt terminations by managing unexpected runtime errors.

