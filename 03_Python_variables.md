# Python Variables – Detailed Notes

## 1. **Introduction to Variables**
- **Definition**: Variables are fundamental elements in programming used to store data that can be referenced and manipulated in a program.
- In Python:
  - Variables are created when a value is assigned.
  - No explicit declaration is needed.
  - Memory allocation happens automatically during assignment.
- **Example**:
  ```python
  a = 100
  ```
  Here, `a` is a variable holding value `100`.

---

## 2. **Declaring and Assigning Variables**
- **Examples**:
  ```python
  age = 32
  height = 6.1
  name = "Krish"
  is_student = True
  ```
- Variables can store integers, floats, strings, booleans, etc.

- **Printing Variables**:
  ```python
  print("Age:", age)
  print("Height:", height)
  print("Name:", name)
  ```

---

## 3. **Naming Conventions**
- **Rules**:
  1. Must be **descriptive**.
  2. Must start with a **letter** or **underscore** (`_`).
  3. Can contain **letters, numbers, underscores**.
  4. **Case-sensitive**.
- **Valid Examples**:
  ```python
  first_name = "Krish"
  last_name = "Nick"
  ```
- **Invalid Examples**:
  ```python
  1age = 30        # starts with number → invalid
  first-name = "Krish"  # dash not allowed → invalid
  @name = "Krish"       # special character → invalid
  ```
- **Case Sensitivity**:
  ```python
  name = "Krish"
  Name = "Nick"
  print(name == Name)  # False
  ```

---

## 4. **Variable Types in Python**
- **Dynamic Typing**: Type is determined at **runtime**.
- Common Types:
  - `int` → Integer numbers
  - `float` → Decimal numbers
  - `str` → Strings
  - `bool` → Boolean values
- **Example**:
  ```python
  age = 25           # int
  height = 6.1       # float
  name = "Krish"     # str
  is_student = True  # bool
  ```
- **Type Checking**:
  ```python
  type(age)  # <class 'int'>
  ```

---

## 5. **Type Conversion (Typecasting)**
- Converting between types:
  ```python
  # int → str
  age_str = str(25)
  
  # str (number) → int
  age_int = int("25")
  
  # float → int
  int_height = int(6.9)  # 6

  # int → float
  float_num = float(5)   # 5.0
  ```
- **Invalid Conversion Example**:
  ```python
  int("Krish")  # Error: invalid literal
  ```

---

## 6. **Dynamic Typing Example**
- Variables can change type during execution:
  ```python
  var = 10
  print(var, type(var))  # int

  var = "Hello"
  print(var, type(var))  # str

  var = 3.14
  print(var, type(var))  # float
  ```

---

## 7. **User Input**
- **Getting input**:
  ```python
  age = input("Enter your age: ")
  print(age, type(age))  # Always str by default
  ```
- **Converting input type**:
  ```python
  age = int(input("Enter your age: "))
  print(age, type(age))  # int
  ```

---

## 8. **Example – Simple Calculator**
```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

sum_val = num1 + num2
diff = num1 - num2
prod = num1 * num2
quot = num1 / num2

print("Sum:", sum_val)
print("Difference:", diff)
print("Product:", prod)
print("Quotient:", quot)
```
**Sample Output**:
```
Enter first number: 56
Enter second number: 10
Sum: 66
Difference: 46
Product: 560
Quotient: 5.6
```

---

## 9. **Key Takeaways**
- Python variables don't need explicit type declaration.
- Naming conventions are crucial for readability.
- Python is dynamically typed.
- Type checking: `type(variable)`
- Typecasting allows converting between data types.
- `input()` always returns a string unless converted.

