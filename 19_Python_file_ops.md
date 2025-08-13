# Python File Operations - Detailed Notes

## **1. Introduction to File Operations in Python**
File handling in Python allows us to create, read, update, and delete files. Python treats files in two primary forms:
- **Text files** (`.txt`): Stores human-readable text.
- **Binary files** (`.bin`): Stores data in binary (byte) format.

Python provides built-in functions and methods to work with files using the `open()` function.

---

## **2. Modes in File Operations**
The `open()` function takes two main parameters:
- **Filename**: Name or path of the file.
- **Mode**: Defines the operation type.

| Mode  | Description |
|-------|-------------|
| `r`   | Read mode (default). Opens the file for reading. File must exist. |
| `w`   | Write mode. Creates a new file or truncates the existing file before writing. |
| `a`   | Append mode. Creates a new file if it doesn't exist, else appends content. |
| `r+`  | Read and write mode. File must exist. |
| `w+`  | Write and read mode. Creates new file or truncates existing file. |
| `a+`  | Append and read mode. Creates new file if not exists. |
| `rb`  | Read binary mode. |
| `wb`  | Write binary mode. |
| `rb+` | Read and write binary mode. |
| `wb+` | Write and read binary mode. |

---

## **3. Using `with open()`**
The `with` statement is preferred because it automatically closes the file after the block is executed.

**Syntax:**
```python
with open("filename.txt", "mode") as file:
    # File operations here
```

Example:
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

## **4. Reading Files**

### **a) Read Entire File**
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
Reads all content into a single string.

### **b) Read Line by Line**
```python
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())  # strip() removes newline characters
```

### **c) Read Specific Number of Characters**
```python
with open("example.txt", "r") as file:
    content = file.read(10)  # Reads first 10 characters
    print(content)
```

---

## **5. Writing Files**

### **a) Write Mode (`w`)**
- Overwrites existing content.
```python
with open("example.txt", "w") as file:
    file.write("Hello World\n")
    file.write("This is a new line.")
```

### **b) Append Mode (`a`)**
- Adds content at the end without removing existing content.
```python
with open("example.txt", "a") as file:
    file.write("\nAppended line.")
```

### **c) Write Multiple Lines**
```python
lines = ["First line\n", "Second line\n", "Third line\n"]
with open("example.txt", "a") as file:
    file.writelines(lines)
```

---

## **6. Binary Files**
Binary files store data in bytes.

### **a) Writing Binary Data**
```python
data = bytes([65, 66, 67])  # ABC in ASCII
with open("example.bin", "wb") as file:
    file.write(data)
```

### **b) Reading Binary Data**
```python
with open("example.bin", "rb") as file:
    content = file.read()
    print(content)
```

---

## **7. Copying Content from One File to Another**
```python
with open("source.txt", "r") as src:
    content = src.read()

with open("destination.txt", "w") as dest:
    dest.write(content)
```

---

## **8. File Cursor Positioning - `seek()`**
- `seek(offset, whence)` moves the cursor.
- `offset`: Position in bytes.
- `whence`:
  - `0` → Start of file
  - `1` → Current position
  - `2` → End of file

Example:
```python
with open("example.txt", "w+") as file:
    file.write("Hello World\nThis is a new text line.")
    file.seek(0)  # Move to start before reading
    content = file.read()
    print(content)
```

---

## **9. Counting Lines, Words, and Characters**
```python
def count_file_stats(filename):
    with open(filename, "r") as file:
        lines = file.readlines()
    line_count = len(lines)
    word_count = sum(len(line.split()) for line in lines)
    char_count = sum(len(line) for line in lines)
    return line_count, word_count, char_count

print(count_file_stats("example.txt"))
```

---

## **10. Key Definitions**
- **File Object**: Python representation of an open file.
- **Text Mode**: File opened for reading/writing strings.
- **Binary Mode**: File opened for reading/writing bytes.
- **Truncation**: Deleting previous content when opening a file in write mode.
- **Append Mode**: Mode that adds data at the end without removing existing data.
- **File Cursor**: Pointer indicating current position in file.

---

## **11. Best Practices**
- Always use `with open()` to ensure files are closed automatically.
- Use `strip()` to clean up newline characters.
- Use append mode to avoid accidental overwriting.
- For large files, read in chunks instead of loading the entire file.
- Always handle exceptions when working with files.

---

✅ **Conclusion:**
We explored all major file operations in Python — reading, writing, appending, binary file handling, copying, and cursor positioning. These concepts are essential for working with persistent data storage in applications.

