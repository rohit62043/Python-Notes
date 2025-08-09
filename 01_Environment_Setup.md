# Creating a Python Virtual Environment — Detailed Notes

## Introduction
- **Common question:** How to create an environment for end-to-end projects?
- **Best practice:** Create a **separate environment for each project** to manage different dependencies and libraries.
- **Problem:** Many people face errors because they don't have **Anaconda** installed — only Python.
- **Goal:** Show **three different ways** to create environments.

---

## **Method 1: Using Python's Built-in `venv` Module**

### Steps
1. **Open terminal** (works in Linux, Windows CMD, or PowerShell).
2. Run the command:
   ```bash
   python -m venv myenv
   ```
   - `myenv` → Name of your environment folder.
3. **Activate the environment:**
   - **Windows:**
     ```bash
     myenv\Scripts\activate
     ```
   - **Linux/Mac:**
     ```bash
     source myenv/bin/activate
     ```
4. **Install packages:**
   ```bash
   pip install pandas
   pip install numpy
   ```
5. **Create a requirements file:**
   ```bash
   pip freeze > requirements.txt
   ```
6. **Check Python version:**
   ```bash
   python --version
   ```
   - Default version is your system Python version.
7. **To use a different Python version:** Download and install from [python.org](https://www.python.org/).
8. **Deactivate:**
   ```bash
   deactivate
   ```

---

## **Method 2: Using `virtualenv`**

### Steps
1. **Install `virtualenv`:**
   ```bash
   pip install virtualenv
   ```
2. **Create environment:**
   ```bash
   virtualenv -p python3 virtual_env
   ```
   - `-p` specifies Python version.
3. **Activate environment:**
   - **Windows:**
     ```bash
     virtual_env\Scripts\activate
     ```
   - **Linux/Mac:**
     ```bash
     source virtual_env/bin/activate
     ```
4. **Install packages:**
   ```bash
   pip install flask
   ```
5. **Deactivate:**
   ```bash
   deactivate
   ```

---

## **Method 3: Using Conda**

### Prerequisite
- Install **Anaconda** or **Miniconda**.

### Steps
1. **Check Python version in base environment:**
   ```bash
   python --version
   ```
2. **Create environment with specific Python version:**
   ```bash
   conda create -p venv1 python=3.10 -y
   ```
   - `-p venv1` → Path or name of environment folder.
   - `python=3.10` → Desired Python version.
   - `-y` → Automatically confirm installation.
3. **Activate environment:**
   ```bash
   conda activate venv1
   ```
4. **Install packages:**
   ```bash
   conda install numpy pandas
   ```
5. **Deactivate:**
   ```bash
   conda deactivate
   ```

### Advantages of Conda
- Easy environment and dependency management.
- Can manage packages for multiple languages.
- GUI support in Anaconda Navigator.

---

## **Summary Table**

| Method        | Prerequisite        | Command to Create | Version Control | Works Without Anaconda |
|--------------|--------------------|-------------------|----------------|------------------------|
| `venv`       | Python installed    | `python -m venv myenv` | System version | ✅ Yes |
| `virtualenv` | Python installed, `pip install virtualenv` | `virtualenv -p pythonX.X env_name` | Custom | ✅ Yes |
| Conda        | Anaconda/Miniconda  | `conda create -p venv1 python=3.10 -y` | Custom | ❌ No |

---

## **Conclusion**
- If you **don’t have Anaconda**, use **`venv`** or **`virtualenv`**.
- If you **do have Anaconda**, **`conda create`** is the most efficient.
- Always activate the environment before installing dependencies.
- Use `requirements.txt` for reproducibility.

