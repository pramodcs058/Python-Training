# Lab 1: Declaring Variables Using Different Literal Types in Python

## Lab Objective
In this lab, you will learn how to:
- Declare variables in Python
- Use integer literals
- Use float literals
- Use boolean literals
- Display variable values using the `print()` function

## Prerequisites
- Python 3.x installed
- Visual Studio Code (or any Python editor)

---

# Step 1: Create a New Python File

1. Open Visual Studio Code.
2. Create a new folder named **PythonLabs**.
3. Inside the folder, create a file named **lab1_literals.py**.

---

# Step 2: Declare Integer Variables

Add the following code:

```python
age = 25
year = 2026

print(age)
print(year)
```

### Run the Program

Open a terminal and execute:

```bash
python lab1_literals.py
```

### Expected Output

```text
25
2026
```

---

# Step 3: Declare Float Variables

Add the following code below the existing code:

```python
salary = 55000.75
temperature = 36.5

print(salary)
print(temperature)
```

### Run the Program

```bash
python lab1_literals.py
```

### Expected Output

```text
55000.75
36.5
```

---

# Step 4: Declare Boolean Variables

Add the following code:

```python
is_active = True
is_admin = False

print(is_active)
print(is_admin)
```

### Run the Program

```bash
python lab1_literals.py
```

### Expected Output

```text
True
False
```

---

# Step 5: Display Variable Names and Values

Replace the print statements with:

```python
age = 25
year = 2026

salary = 55000.75
temperature = 36.5

is_active = True
is_admin = False

print("Age:", age)
print("Year:", year)
print("Salary:", salary)
print("Temperature:", temperature)
print("Active User:", is_active)
print("Administrator:", is_admin)
```

### Run the Program

```bash
python lab1_literals.py
```

### Sample Output

```text
Age: 25
Year: 2026
Salary: 55000.75
Temperature: 36.5
Active User: True
Administrator: False
```

---

# Step 6: Verify Data Types

Add the following code:

```python
print(type(age))
print(type(salary))
print(type(is_active))
```

### Run the Program

```bash
python lab1_literals.py
```

### Expected Output

```text
<class 'int'>
<class 'float'>
<class 'bool'>
```

---

# Challenge Exercise

Create three new variables:

```python
number_of_students = 30
product_price = 1499.99
is_course_completed = False
```

Display their values and data types.

---

# Knowledge Check

1. Which literal type is used to store whole numbers?
2. Which literal type is used to store decimal numbers?
3. What are the two possible Boolean values in Python?
4. What function is used to display output on the screen?

---

# Summary

In this lab, you learned how to:
- Create variables in Python
- Use integer literals (`int`)
- Use float literals (`float`)
- Use boolean literals (`bool`)
- Display values using `print()`
- Verify variable types using `type()`
