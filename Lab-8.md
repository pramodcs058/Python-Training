# Lab 8: Read String Input and Cast to Numeric Types for Calculations

## Lab Objective

In this lab, you will learn how to:

- Read user input using the `input()` function
- Understand that all input is initially received as a string
- Convert string input into different Python data types
- Perform calculations using `int` and `float`
- Explore additional type conversions such as `bool`, `complex`, and `str`
- Handle common type conversion scenarios used in data processing applications

---

# Prerequisites

Before starting this lab, you should know:

- Variables
- Data types
- The `input()` function
- Basic arithmetic operators

---

# Understanding User Input

When Python receives input from a user, the value is always stored as a string.

Example:

```python
age = input("Enter your age: ")
```

Even if the user enters:

```text
25
```

Python stores:

```python
"25"
```

To perform calculations, you must convert the value into an appropriate numeric type.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab8_type_casting.py
```

---

# Step 2: Read Input as a String

Add the following code:

```python
user_input = input("Enter a value: ")

print("Value:", user_input)
print("Data Type:", type(user_input))
```

### Run the Program

```bash
python lab8_type_casting.py
```

### Sample Output

```text
Enter a value: 100

Value: 100
Data Type: <class 'str'>
```

---

# Step 3: Convert String to Integer

Replace the code with:

```python
age = int(input("Enter your age: "))

years_after_five = age + 5

print("Current Age:", age)
print("Age After 5 Years:", years_after_five)
```

### Run the Program

```bash
python lab8_type_casting.py
```

### Sample Output

```text
Enter your age: 30

Current Age: 30
Age After 5 Years: 35
```

---

# Step 4: Convert String to Float

Replace the code with:

```python
salary = float(
    input("Enter your monthly salary: ")
)

annual_salary = salary * 12

print("Annual Salary:", annual_salary)
```

### Sample Output

```text
Enter your monthly salary: 50000.50

Annual Salary: 600006.0
```

---

# Step 5: Perform Calculations Using Multiple Numeric Inputs

Add the following code:

```python
number_1 = int(input("Enter first number: "))
number_2 = int(input("Enter second number: "))

sum_result = number_1 + number_2
product_result = number_1 * number_2

print("Sum:", sum_result)
print("Product:", product_result)
```

### Sample Output

```text
Enter first number: 10
Enter second number: 20

Sum: 30
Product: 200
```

---

# Step 6: Convert Input to a Float for Scientific Calculations

Add the following code:

```python
radius = float(input("Enter radius: "))

area = 3.14159 * radius * radius

print("Area of Circle:", area)
```

### Sample Output

```text
Enter radius: 5.5

Area of Circle: 95.0330975
```

---

# Step 7: Convert String Input to Boolean

Add the following code:

```python
subscription_status = bool(
    input("Enter subscription status: ")
)

print("Boolean Value:", subscription_status)
```

### Sample Output

```text
Enter subscription status: Yes

Boolean Value: True
```

### Important Note

Any non-empty string becomes:

```python
True
```

Only an empty string becomes:

```python
False
```

Example:

```python
bool("Python")   # True
bool("")         # False
```

---

# Step 8: Convert String Input to Complex Numbers

Add the following code:

```python
complex_number = complex(
    input("Enter a complex number: ")
)

print("Complex Value:", complex_number)
print("Data Type:", type(complex_number))
```

### Sample Output

```text
Enter a complex number: 3+4j

Complex Value: (3+4j)
Data Type: <class 'complex'>
```

---

# Step 9: Explore Common Type Conversions

Add the following code:

```python
number_text = "150"

integer_value = int(number_text)
float_value = float(number_text)
string_value = str(integer_value)
boolean_value = bool(integer_value)

print("Integer:", integer_value)
print("Float:", float_value)
print("String:", string_value)
print("Boolean:", boolean_value)
```

### Expected Output

```text
Integer: 150
Float: 150.0
String: 150
Boolean: True
```

---

# Step 10: Build a Mini Data Processing Calculator

Replace the code with:

```python
employee_name = input(
    "Enter employee name: "
)

hours_worked = float(
    input("Enter hours worked: ")
)

hourly_rate = float(
    input("Enter hourly rate: ")
)

total_salary = (
    hours_worked * hourly_rate
)

print("\n--- Employee Payroll Report ---")
print("Employee:", employee_name)
print("Hours Worked:", hours_worked)
print("Hourly Rate:", hourly_rate)
print("Total Salary:", total_salary)
```

### Sample Output

```text
Enter employee name: Rahul
Enter hours worked: 40
Enter hourly rate: 500

--- Employee Payroll Report ---
Employee: Rahul
Hours Worked: 40.0
Hourly Rate: 500.0
Total Salary: 20000.0
```

---

# Step 11: Verify Data Types

Add the following code:

```python
value = input("Enter any value: ")

print(type(value))
print(type(int(value)))
print(type(float(value)))
```

### Sample Output

```text
Enter any value: 100

<class 'str'>
<class 'int'>
<class 'float'>
```

---

# Challenge Exercise

Create a program that:

1. Accepts:
   - Product Name
   - Product Price
   - Quantity

2. Converts the inputs to appropriate data types.

3. Calculates:

```text
Total Cost = Product Price × Quantity
```

4. Displays a formatted purchase summary.

Example:

```text
Product: Laptop
Price: 50000
Quantity: 2
Total Cost: 100000
```

---

# Knowledge Check

1. What data type does `input()` return?
2. Why is type casting required?
3. When should you use `int()`?
4. When should you use `float()`?
5. What happens when `bool()` receives a non-empty string?
6. Which function converts a value into a complex number?
7. What error occurs if you try to convert non-numeric text into an integer?

---

# Summary

In this lab, you learned how to:

- Read user input as strings
- Convert strings to integers using `int()`
- Convert strings to floating-point numbers using `float()`
- Convert values to booleans using `bool()`
- Convert values to complex numbers using `complex()`
- Perform calculations using converted values
- Verify data types using `type()`
- Build practical data-processing applications using type casting

Type conversion is a fundamental skill used in data engineering, analytics, ETL pipelines, web applications, APIs, and business applications.
