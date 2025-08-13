# Python Standard Library Overview – Comprehensive Notes

Python's **Standard Library** is a vast collection of modules and packages included with Python, offering built-in solutions for common programming tasks.

---

## 1. **`array` Module**
**Definition:** A module that provides a space-efficient storage of basic data types (like integers and floats) in a contiguous memory layout.

**Syntax:**
```python
import array
arr = array.array('i', [1, 2, 3, 4])
print(arr)
```
**Type Codes:**
- `'i'` – Integer
- `'f'` – Float
- `'d'` – Double

**More Examples:**
```python
arr.append(5)
arr.extend([6, 7])
print(arr[0], arr[-1])
```
**Use Cases:**
- Storing large volumes of numbers efficiently.
- Interfacing with C code.

---

## 2. **`math` Module**
**Definition:** Provides access to mathematical functions and constants defined by the C standard.
```python
import math
print(math.sqrt(25))
print(math.ceil(4.2))
print(math.floor(4.8))
print(math.factorial(5))
```
**Use Cases:**
- Trigonometry: `math.sin`, `math.cos`
- Constants: `math.pi`, `math.e`

---

## 3. **`random` Module**
**Definition:** Implements pseudo-random number generators for various distributions.
```python
import random
print(random.randint(1, 10))
print(random.choice(['apple', 'banana', 'cherry']))
print(random.sample(range(10), 3))
```
**Use Cases:**
- Generating random passwords.
- Simulating dice rolls.

---

## 4. **`os` Module**
**Definition:** Provides functions for interacting with the operating system, such as file/directory manipulation and process management.
```python
import os
print(os.getcwd())
os.mkdir("test_dir")
print(os.listdir())
os.rename("test_dir", "renamed_dir")
```
**Use Cases:**
- Automating file management.
- Environment variable handling: `os.environ`

---

## 5. **`shutil` Module**
**Definition:** Offers high-level file operations like copying, moving, and removing files/directories.
```python
import shutil
shutil.copyfile("source.txt", "destination.txt")
shutil.move("destination.txt", "new_location.txt")
```
**Use Cases:**
- Backup creation.
- Moving/duplicating directory trees.

---

## 6. **`json` Module**
**Definition:** Enables encoding and decoding data in JSON format.
```python
import json
data = {"name": "Krish", "age": 25}
json_str = json.dumps(data, indent=4)
print(json_str)
parsed = json.loads(json_str)
print(parsed["name"])
```
**Use Cases:**
- API responses.
- Config file parsing.

---

## 7. **`csv` Module**
**Definition:** Provides functionality to read from and write to CSV (Comma-Separated Values) files.
```python
import csv
# Writing
with open('example.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(['Name', 'Age'])
    writer.writerow(['Krish', 32])
# Reading
with open('example.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```
**Use Cases:**
- Data export/import.
- Spreadsheet automation.

---

## 8. **`datetime` Module**
**Definition:** Supplies classes for manipulating dates and times.
```python
from datetime import datetime, timedelta
now = datetime.now()
yesterday = now - timedelta(days=1)
print("Now:", now)
print("Yesterday:", yesterday)
```
**Use Cases:**
- Event scheduling.
- Logging with timestamps.

---

## 9. **`time` Module**
**Definition:** Provides time-related functions for tracking and controlling execution.
```python
import time
start = time.time()
time.sleep(2)
end = time.time()
print("Elapsed time:", end - start)
```
**Use Cases:**
- Code profiling.
- Delays in automation scripts.

---

## 10. **`re` Module**
**Definition:** Offers regular expression matching operations for strings.
```python
import re
pattern = r'\d+'
text = 'Order 123 has been shipped.'
match = re.search(pattern, text)
if match:
    print("Found number:", match.group())
```
**Use Cases:**
- Input validation (emails, phone numbers).
- Data cleaning and extraction.

---

## Summary Table
| Module     | Purpose | Example Use Case |
|------------|---------|------------------|
| `array`    | Numeric storage | Store integers efficiently |
| `math`     | Math functions | Geometry calculations |
| `random`   | Random values | Game dice roll |
| `os`       | OS operations | Directory creation |
| `shutil`   | File ops | Backup files |
| `json`     | JSON handling | API parsing |
| `csv`      | CSV handling | Export sales data |
| `datetime` | Dates/times | Scheduling |
| `time`     | Time control | Delay execution |
| `re`       | Regex | Email validation |

