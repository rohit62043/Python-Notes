# **Python Dictionaries – Detailed Notes**

## **1. Introduction**
- **Definition**:  
  A dictionary is an **unordered collection of items** in **key–value pairs**.
- **Properties**:
  - Keys must be **unique** and **immutable** (e.g., strings, numbers, tuples).
  - Values can be of **any type** and **mutable**.
  - Dictionary data is stored as:  
    ```python
    { key1: value1, key2: value2, ... }
    ```
  - Accessed using keys instead of indexes.
- **Real-world analogy**: Like a **real dictionary** where the word is the **key** and the meaning is the **value**.

---

## **2. Creating Dictionaries**

### **Empty Dictionaries**
```python
# Method 1 – Using {}
empty_dict = {}
print(type(empty_dict))  # <class 'dict'>

# Method 2 – Using dict()
empty_dict2 = dict()
```

### **With Key–Value Pairs**
```python
student = {
    "name": "Krish",
    "age": 32,
    "grade": "A"
}
```

- **Duplicate keys** → later value replaces earlier value:
```python
student = {"name": "Krish", "name": 24}
print(student)  # {'name': 24}
```

---

## **3. Accessing Dictionary Elements**

### **Direct Access**
```python
print(student["grade"])  # A
```
> ⚠️ Raises `KeyError` if key is missing.

### **Using `.get()` Method**
```python
print(student.get("grade"))        # A
print(student.get("last_name"))    # None
print(student.get("last_name", "Not Available"))  # Not Available
```
> `.get()` is safer — avoids errors and allows a default value.

---

## **4. Modifying Dictionary Elements**

- **Dictionaries are mutable** — you can add, update, or delete elements.

### **Update an Existing Key**
```python
student["age"] = 33
```

### **Add a New Key–Value Pair**
```python
student["address"] = "India"
```

### **Delete a Key**
```python
del student["grade"]
```

---

## **5. Common Dictionary Methods**

| Method                      | Description |
|-----------------------------|-------------|
| `dict.keys()`               | Returns all keys. |
| `dict.values()`             | Returns all values. |
| `dict.items()`              | Returns list of `(key, value)` tuples. |
| `dict.copy()`               | Returns a **shallow copy** of the dictionary. |

**Example**:
```python
keys = student.keys()
values = student.values()
items = student.items()
```

---

## **6. Shallow Copy vs Direct Assignment**

```python
# Direct assignment (same memory reference)
copy1 = student
copy1["name"] = "Krish2"
print(student["name"])  # Krish2

# Shallow copy (different memory reference)
copy2 = student.copy()
copy2["name"] = "Krish3"
print(student["name"])  # Krish2 (unchanged)
```

---

## **7. Iterating Over Dictionaries**

### **Keys**
```python
for key in student.keys():
    print(key)
```

### **Values**
```python
for value in student.values():
    print(value)
```

### **Key–Value Pairs**
```python
for key, value in student.items():
    print(f"{key}: {value}")
```

---

## **8. Nested Dictionaries**

**Creating:**
```python
students = {
    "student1": {"name": "Krish", "age": 32},
    "student2": {"name": "Peter", "age": 35}
}
```

**Accessing Nested Values:**
```python
print(students["student2"]["name"])  # Peter
print(students["student2"]["age"])   # 35
```

**Iterating Over Nested Dictionaries:**
```python
for student_id, student_info in students.items():
    print(student_id, student_info)
    for key, value in student_info.items():
        print(f"{key}: {value}")
```

---

## **9. Dictionary Comprehension**

**Syntax:**
```python
{ key_expr: value_expr for item in iterable if condition }
```

**Example – Squares Dictionary:**
```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

## **10. Common Errors**
- **KeyError** — occurs when accessing a non-existent key via `dict[key]`.
- **Unhashable key** — occurs if a mutable type (like a list) is used as a key.

---

✅ **Key Takeaways**
- Use `.get()` for safer key access.
- Remember that dictionaries are mutable — changes affect references.
- Use `.copy()` to avoid unintended reference sharing.
- Nested dictionaries are common in JSON and NoSQL databases.
- Dictionary comprehension is a powerful shorthand for creating dictionaries.

