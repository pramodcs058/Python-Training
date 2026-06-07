# Lab 4: Refactor Poorly Named Variables to Follow PEP 8 Standards

## Lab Objective

In this lab, you will learn how to:

- Identify poorly named variables in Python code
- Understand Python PEP 8 naming conventions
- Refactor variable names to improve readability
- Make data-processing scripts easier to maintain
- Apply consistent naming standards in real-world projects

---

# Prerequisites

Before starting this lab, you should know:

- Python variables
- Basic Python syntax
- Reading and modifying Python scripts

---

# What is PEP 8?

PEP 8 is the official Python Style Guide.

For variable names, PEP 8 recommends:

✅ Use lowercase letters

✅ Separate words using underscores

```python
employee_salary = 50000
customer_name = "John"
```

❌ Avoid unclear names

```python
x = 50000
EMP = "John"
cNm = "John"
```

Good variable names make code easier to understand and maintain.

---

# Scenario

You have received a data-processing script from another developer.

The script works correctly but uses poor variable names.

Your task is to refactor the script to follow PEP 8 standards without changing its functionality.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab4_refactor_variables.py
```

---

# Step 2: Review the Original Script

Add the following code:

```python
EmpNm = "Alice"
EmpAge = 30
EmpSal = 65000

print(EmpNm)
print(EmpAge)
print(EmpSal)
```

### Questions

What do these variable names mean?

Can a new developer understand them immediately?

---

# Step 3: Run the Original Script

Execute:

```bash
python lab4_refactor_variables.py
```

### Expected Output

```text
Alice
30
65000
```

Notice that the program works correctly.

However, the variable names are not very descriptive.

---

# Step 4: Refactor Using PEP 8 Standards

Replace the code with:

```python
employee_name = "Alice"
employee_age = 30
employee_salary = 65000

print(employee_name)
print(employee_age)
print(employee_salary)
```

### Run the Program

```bash
python lab4_refactor_variables.py
```

### Expected Output

```text
Alice
30
65000
```

### Observation

The output remains the same.

The code is now easier to read and understand.

---

# Step 5: Refactor a Data Processing Script

Review the following poorly named script:

```python
Nm = "Laptop"
Qty = 5
Pr = 45000

Tot = Qty * Pr

print(Nm)
print(Tot)
```

### Task

Refactor it using meaningful names.

### Solution

```python
product_name = "Laptop"
quantity = 5
price = 45000

total_amount = quantity * price

print(product_name)
print(total_amount)
```

---

# Step 6: Refactor Multiple Variables

Add the following code:

```python
CustNm = "Rahul"
OrdCnt = 12
OrdVal = 24000

print(CustNm)
print(OrdCnt)
print(OrdVal)
```

### Your Task

Rename the variables to:

```python
customer_name
order_count
order_value
```

Run the script again and verify that the output remains unchanged.

---

# Step 7: Compare Before and After

### Before Refactoring

```python
EmpNm = "Alice"
EmpAge = 30
EmpSal = 65000
```

### After Refactoring

```python
employee_name = "Alice"
employee_age = 30
employee_salary = 65000
```

### Benefits

- Easier to understand
- Easier to maintain
- Easier to debug
- Follows industry standards
- Improves team collaboration

---

# Step 8: Refactor a Mini Data Report

Add the following code:

```python
StuNm = "Priya"
M1 = 85
M2 = 90
M3 = 88

Tot = M1 + M2 + M3
Avg = Tot / 3

print(StuNm)
print(Tot)
print(Avg)
```

### Refactor It

Expected variable names:

```python
student_name
math_score
science_score
english_score
total_marks
average_marks
```

### Verify

Run:

```bash
python lab4_refactor_variables.py
```

Ensure the output remains unchanged.

---

# Challenge Exercise

Refactor the following script:

```python
ProdNm = "Keyboard"
ProdQty = 10
ProdPr = 1500

TotAmt = ProdQty * ProdPr

print(ProdNm)
print(TotAmt)
```

### Requirements

Rename variables using PEP 8 naming conventions.

Suggested names:

```python
product_name
product_quantity
product_price
total_amount
```

---

# Knowledge Check

1. What is PEP 8?
2. Which naming style is recommended for Python variables?
3. Why is `employee_salary` better than `EmpSal`?
4. Does refactoring variable names change program functionality?
5. What is the benefit of meaningful variable names?

---

# Summary

In this lab, you learned how to:

- Identify poorly named variables
- Apply PEP 8 naming conventions
- Use descriptive variable names
- Improve code readability and maintainability
- Refactor existing Python scripts without changing functionality

Following PEP 8 standards helps create professional, readable, and maintainable Python code.
