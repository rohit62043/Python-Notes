# Python Control Flow - Conditional Statements

## 1. Introduction to Conditional Statements
- **Definition:** Conditional statements control the flow of execution based on certain conditions.
- **Purpose:** Execute specific blocks of code only if given conditions evaluate to `True`.
- **Types in Python:**
  - `if`
  - `else`
  - `elif`
  - Nested conditional statements

---

## 2. The `if` Statement
- **Definition:** Evaluates a condition and executes the block of code inside it if the condition is `True`.
- **Syntax:**
  ```python
  if condition:
      # code block
  ```
- **Example:**
  ```python
  age = 20
  if age >= 18:
      print("You are allowed to vote in the elections")
  ```
- **Key Points:**
  - Uses **indentation** to define code blocks.
  - Condition must return a boolean value (`True` or `False`).

---

## 3. The `else` Statement
- **Definition:** Executes a block of code if the `if` condition is `False`.
- **Syntax:**
  ```python
  if condition:
      # code block
  else:
      # code block if condition is False
  ```
- **Example:**
  ```python
  age = 16
  if age >= 18:
      print("You are eligible for voting")
  else:
      print("You are a minor")
  ```

---

## 4. The `elif` Statement
- **Definition:** Stands for "else if" and allows checking multiple conditions.
- **Syntax:**
  ```python
  if condition1:
      # code block
  elif condition2:
      # code block
  else:
      # code block
  ```
- **Example:**
  ```python
  age = 20
  if age < 13:
      print("You are a child")
  elif age < 18:
      print("You are a teenager")
  else:
      print("You are an adult")
  ```

---

## 5. Nested Conditional Statements
- **Definition:** Placing one or more `if`, `elif`, or `else` statements inside another conditional block.
- **Purpose:** Check multiple related conditions with structured logic.
- **Example:**
  ```python
  num = int(input("Enter the number: "))

  if num > 0:
      print("The number is positive")
      if num % 2 == 0:
          print("The number is even")
      else:
          print("The number is odd")
  else:
      print("The number is zero or negative")
  ```
- **Indentation:** Crucial for correct execution.

---

## 6. Practical Example - Leap Year Checker
- **Logic:**
  - A year is a leap year if:
    1. Divisible by 4 **and** not divisible by 100, **or**
    2. Divisible by 400
- **Example Code:**
  ```python
  year = int(input("Enter the year: "))

  if year % 4 == 0:
      if year % 100 == 0:
          if year % 400 == 0:
              print(f"{year} is a leap year")
          else:
              print(f"{year} is not a leap year")
      else:
          print(f"{year} is a leap year")
  else:
      print(f"{year} is not a leap year")
  ```

---

## 7. Common Errors & Best Practices
- **Errors:**
  - Missing colon (`:`) after condition.
  - Incorrect indentation.
  - Misusing comparison operators (`=` vs `==`).
- **Best Practices:**
  - Keep conditions simple and readable.
  - Use parentheses for clarity.
  - Maintain consistent indentation.

---

## 8. Assignments & Practice Problems

### 8.1 Simple Calculator
- **Objective:** Take user input for two numbers and an operation (`+`, `-`, `*`, `/`, `%`), then perform the calculation using `if-elif-else`.
- **Example Structure:**
  ```python
  num1 = float(input("Enter first number: "))
  num2 = float(input("Enter second number: "))
  operation = input("Enter operation (+, -, *, /, %): ")

  if operation == "+":
      print(num1 + num2)
  elif operation == "-":
      print(num1 - num2)
  elif operation == "*":
      print(num1 * num2)
  elif operation == "/":
      if num2 != 0:
          print(num1 / num2)
      else:
          print("Division by zero is not allowed")
  elif operation == "%":
      print(num1 % num2)
  else:
      print("Invalid operation")
  ```

### 8.2 Ticket Price Determination
- **Objective:** Determine ticket price based on age and student status.
- **Conditions:**
  - Age < 5 → Free
  - Age < 12 → $10
  - Age < 17 → $12 (if student), else $15
  - Else → $20
- **Example Structure:**
  ```python
  age = int(input("Enter your age: "))
  student = input("Are you a student (yes/no)?: ").lower()

  if age < 5:
      price = 0
  elif age < 12:
      price = 10
  elif age < 17:
      if student == "yes":
          price = 12
      else:
          price = 15
  else:
      price = 20

  print(f"Ticket price: ${price}")
  ```

