# Lab 9: Handle Invalid Input Gracefully Using Basic Error Checks

## Lab Objective

In this lab, you will learn how to:

- Identify common user input errors
- Validate user input before processing it
- Handle invalid numeric input gracefully
- Use `try` and `except` blocks for error handling
- Create more reliable and user-friendly programs
- Apply basic input validation techniques used in real-world applications

---

# Prerequisites

Before starting this lab, you should know:

- Variables and data types
- User input using `input()`
- Type casting using `int()` and `float()`
- Basic arithmetic operations

---

# Why Input Validation Matters

Users do not always enter the expected values.

Examples:

Expected:

```text
25
```

User enters:

```text
twenty five
```

or

```text
25abc
```

Without validation, the program may crash.

Good applications validate input and display meaningful error messages.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab9_input_validation.py
```

---

# Step 2: Observe an Input Error

Add the following code:

```python
age = int(input("Enter your age: "))

print("Age:", age)
```

### Run the Program

```bash
python lab9_input_validation.py
```

Enter:

```text
abc
```

### Result

```text
ValueError: invalid literal for int()
```

The application terminates unexpectedly.

---

# Step 3: Handle Invalid Integer Input

Replace the code with:

```python
try:
    age = int(input("Enter your age: "))
    print("Age:", age)

except ValueError:
    print("Invalid input. Please enter a whole number.")
```

### Run the Program

```bash
python lab9_input_validation.py
```

### Sample Execution

```text
Enter your age: abc

Invalid input. Please enter a whole number.
```

### Observation

The program no longer crashes.

---

# Step 4: Handle Invalid Decimal Input

Add the following code:

```python
try:
    salary = float(
        input("Enter your salary: ")
    )

    print("Salary:", salary)

except ValueError:
    print("Invalid salary value.")
```

### Sample Execution

```text
Enter your salary: fifty thousand

Invalid salary value.
```

---

# Step 5: Validate Positive Numbers

Replace the code with:

```python
try:
    quantity = int(
        input("Enter quantity: ")
    )

    if quantity > 0:
        print("Quantity Accepted")
    else:
        print("Quantity must be greater than zero")

except ValueError:
    print("Please enter a valid integer")
```

### Sample Output

```text
Enter quantity: -5

Quantity must be greater than zero
```

---

# Step 6: Validate Temperature Input

Add the following code:

```python
try:
    temperature = float(
        input("Enter temperature in Celsius: ")
    )

    if temperature < -273.15:
        print(
            "Temperature cannot be below absolute zero"
        )
    else:
        print(
            "Temperature Recorded:",
            temperature
        )

except ValueError:
    print("Invalid temperature value")
```

### Sample Output

```text
Enter temperature in Celsius: -500

Temperature cannot be below absolute zero
```

---

# Step 7: Validate Distance Input

Add the following code:

```python
try:
    distance_km = float(
        input("Enter distance in KM: ")
    )

    if distance_km < 0:
        print(
            "Distance cannot be negative"
        )
    else:
        print(
            "Distance Accepted"
        )

except ValueError:
    print("Invalid distance value")
```

---

# Step 8: Build a Safe Calculator

Add the following code:

```python
try:
    number_1 = float(
        input("Enter first number: ")
    )

    number_2 = float(
        input("Enter second number: ")
    )

    result = number_1 + number_2

    print("Result:", result)

except ValueError:
    print(
        "Please enter valid numeric values"
    )
```

### Sample Execution

```text
Enter first number: 10
Enter second number: xyz

Please enter valid numeric values
```

---

# Step 9: Validate Employee Payroll Input

Replace the code with:

```python
try:
    employee_name = input(
        "Enter employee name: "
    )

    hours_worked = float(
        input("Enter hours worked: ")
    )

    hourly_rate = float(
        input("Enter hourly rate: ")
    )

    if hours_worked < 0:
        print("Hours cannot be negative")

    elif hourly_rate < 0:
        print("Hourly rate cannot be negative")

    else:
        total_salary = (
            hours_worked * hourly_rate
        )

        print("\nPayroll Report")
        print("Employee:", employee_name)
        print("Salary:", total_salary)

except ValueError:
    print(
        "Please enter valid numeric values"
    )
```

### Sample Output

```text
Enter employee name: Rahul
Enter hours worked: 40
Enter hourly rate: 500

Payroll Report
Employee: Rahul
Salary: 20000.0
```

---

# Step 10: Create a Retry Mechanism

Add the following code:

```python
while True:

    try:
        age = int(
            input("Enter your age: ")
        )

        print("Age Recorded:", age)
        break

    except ValueError:
        print(
            "Invalid input. Try again."
        )
```

### Sample Execution

```text
Enter your age: abc
Invalid input. Try again.

Enter your age: xyz
Invalid input. Try again.

Enter your age: 30
Age Recorded: 30
```

### Observation

The user continues until valid input is provided.

---

# Challenge Exercise

Create a program that:

1. Accepts:
   - Product Name
   - Product Price
   - Quantity

2. Validates:

   - Price must be numeric
   - Quantity must be a positive integer

3. Calculates:

```text
Total Cost = Price × Quantity
```

4. Displays meaningful error messages if invalid data is entered.

---

# Real-World Applications

Input validation is used in:

- Data entry forms
- ETL pipelines
- Web applications
- APIs
- Banking systems
- Payroll systems
- Inventory management applications

Without validation, bad data can corrupt business processes.

---

# Knowledge Check

1. What exception occurs when `int()` fails?
2. What exception occurs when `float()` fails?
3. Why is input validation important?
4. What is the purpose of a `try` block?
5. What is the purpose of an `except` block?
6. How can you repeatedly prompt users until valid input is entered?

---

# Summary

In this lab, you learned how to:

- Detect invalid user input
- Prevent application crashes
- Handle exceptions using `try` and `except`
- Validate numeric ranges and business rules
- Create retry mechanisms for user input
- Build robust data-processing applications

Input validation is a critical skill for Python developers, data engineers, analysts, and application developers because real-world data is rarely perfect.
