# Detailed Notes on Python `os` Module for File and Directory Operations

## 1. Creating a New Directory
- **Import Requirement**: `import os`
- **Function Used**: `os.mkdir(directory_name)`
- **Example**:
  ```python
  import os
  new_dir = "package"
  os.mkdir(new_dir)
  print(f"Directory {new_dir} created")
  ```
- Creates a new folder in the current working directory.

---

## 2. Listing Files and Directories
- **Function Used**: `os.listdir(path)`
- `path` can be `"."` for current working directory.
- **Example**:
  ```python
  items = os.listdir('.')
  print(items)
  ```
- Returns a list of all files and folders in the specified directory.

---

## 3. Joining Paths
- **Why Important**: Avoids OS-specific path formatting issues.
- **Function Used**: `os.path.join()`
- **Example**:
  ```python
  dir_name = "folder"
  file_name = "file.txt"
  full_path = os.path.join(dir_name, file_name)
  print(full_path)
  ```
- Can also combine with `os.getcwd()` for absolute paths:
  ```python
  full_path_abs = os.path.join(os.getcwd(), dir_name, file_name)
  print(full_path_abs)
  ```

---

## 4. Checking Path Existence
- **Function Used**: `os.path.exists(path)`
- **Example**:
  ```python
  if os.path.exists("example1.txt"):
      print("Path exists")
  else:
      print("Path does not exist")
  ```
- Useful before performing file operations to prevent errors.

---

## 5. Checking if Path is File or Directory
- **Functions Used**:
  - `os.path.isfile(path)` → True if path is a file.
  - `os.path.isdir(path)` → True if path is a directory.
- **Example**:
  ```python
  path = "example.txt"
  if os.path.isfile(path):
      print("It is a file")
  elif os.path.isdir(path):
      print("It is a directory")
  else:
      print("Path is neither a file nor a directory")
  ```

---

## 6. Relative vs Absolute Paths
- **Relative Path**: Path from current working directory (e.g., `folder/file.txt`).
- **Absolute Path**: Full path from the root of the filesystem.

---

## 7. Getting Absolute Path
- **Function Used**: `os.path.abspath(relative_path)`
- **Example**:
  ```python
  relative_path = "example.txt"
  absolute_path = os.path.abspath(relative_path)
  print(absolute_path)
  ```
- Directly returns the complete path without manually joining parts.

---

## Key Points
- Always use `os.path.join()` for building paths.
- Use `os.path.exists()` before accessing a file or directory.
- Distinguish between files and directories using `isfile()` and `isdir()`.
- `os.path.abspath()` is a quick way to convert relative paths to absolute.

---

**Practice Tip**: Combine these functions to build scripts that can dynamically create, check, and manage files/folders across different operating systems.

