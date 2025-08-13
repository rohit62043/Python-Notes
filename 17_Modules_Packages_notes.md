# Python Modules and Packages — Detailed Notes

## 1. Introduction

- **Modules**: Single Python files containing functions, classes, and variables.
- **Packages**: Directories containing one or more modules, along with a special `__init__.py` file.
- **Functions**: Blocks of reusable code that perform a specific task.
- **Namespace**: A container that holds names (identifiers) and maps them to objects.
- **Alias**: An alternate name given to a package or module for convenience.
- Python is an **open-source programming language** with numerous built-in and third-party packages.

---

## 2. Importing Packages

**Import**: Bringing external code (from modules or packages) into the current Python script.

### 2.1 Syntax

```python
import package_name
from package_name import function_name
from package_name import *  # Import all functions
import package_name as alias  # Use alias for shorter reference
```

### 2.2 Example — Importing Built-in `math` Module

```python
import math
result = math.sqrt(16)  # Square root of 16
```

**Import specific functions:**

```python
from math import sqrt, pi
print(sqrt(25))  # 5.0
print(pi)        # 3.141592653589793
```

**Import all functions:**

```python
from math import *
print(sqrt(16))
print(pi)
```

---

## 3. Installing External Packages

Some packages (e.g., NumPy, Pandas) are **not installed by default**.

**Installation Methods:**

1. **Using pip directly** — `pip` is Python’s package installer.

```bash
pip install numpy
```

2. **Using **``** file**

```bash
pip install -r requirements.txt
```

Example `requirements.txt`:

```
numpy
```

**Alias Usage:**

```python
import numpy as np
arr = np.array([1, 2, 3, 4])
```

---

## 4. Creating a Custom Package

### 4.1 Folder Structure

```
project_folder/
│
├── packages/
│   ├── __init__.py        # Makes 'packages' a package
│   ├── maths.py           # Module file
│
└── test.py                # Script to test imports
```

### 4.2 Special `__init__.py` File

- Marks a folder as a **Python package**.
- Can be empty or contain initialization code.
- **Special File**: A file with double underscores used for special purposes in Python.

```python
# __init__.py
"""
This file makes the folder a Python package.
"""
```

---

### 4.3 Creating a Module

```python
# maths.py
def addition(a, b):
    return a + b

def subtraction(a, b):
    return a - b
```

### 4.4 Importing Custom Modules

**Method 1 — Import specific functions:**

```python
from packages.maths import addition
print(addition(2, 3))
```

**Method 2 — Import the whole module:**

```python
from packages import maths
print(maths.subtraction(4, 3))
```

**Method 3 — Import all functions:**

```python
from packages.maths import *
print(addition(2, 3))
print(subtraction(4, 3))
```

---

## 5. Running the Script

Ensure you are in the correct directory:

```bash
cd project_folder
python test.py
```

Example `test.py`:

```python
from packages.maths import *
print(addition(2, 3))       # 5
print(subtraction(4, 3))    # 1
```

---

## 6. Sub-Packages

**Sub-package**: A package inside another package.

### 6.1 Folder Structure

```
packages/
│
├── __init__.py
├── maths.py
└── sub_package/
    ├── __init__.py
    └── mult.py
```

### 6.2 Example `mult.py`

```python
def multiply(a, b):
    return a * b
```

### 6.3 Importing from Sub-Packages

```python
from packages.sub_package.mult import multiply
print(multiply(4, 5))  # 20
```

---

## 7. Summary

- **Modules**: Single Python files containing reusable code.
- **Packages**: Directories containing modules and `__init__.py`.
- **Sub-packages**: Packages within other packages.
- **Functions**: Code blocks for specific tasks.
- **Namespace**: Isolated space for names to avoid conflicts.
- **Alias**: Short name for easier usage of a module.
- Import methods: `import`, `from ... import`, `import as`, `from ... import *`.
- External packages require installation via `pip`.
- Custom packages improve project structure and reusability.

