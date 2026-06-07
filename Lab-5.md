# Lab 5: Emphasize Clarity in Naming for Data Pipelines and Transformation Scripts

## Lab Objective

In this lab, you will learn how to:

- Use meaningful names in data pipeline scripts
- Improve readability of data transformation code
- Apply PEP 8 naming conventions
- Refactor unclear variable names into descriptive names
- Make data processing workflows easier to understand and maintain

---

# Prerequisites

Before starting this lab, you should know:

- Python variables
- Basic calculations and assignments
- PEP 8 variable naming conventions
- Simple data processing concepts

---

# Why Naming Matters in Data Pipelines

Data pipelines often contain multiple stages such as:

1. Data Ingestion
2. Data Cleaning
3. Data Transformation
4. Data Validation
5. Data Reporting

Poor variable names make it difficult to understand:

- What data is being processed
- Which transformation is occurring
- What the output represents

Clear names improve:

- Maintainability
- Collaboration
- Troubleshooting
- Code reviews

---

# Scenario

You have inherited a data transformation script from another developer.

The script works correctly, but the variable names are unclear.

Your task is to improve the naming while keeping the functionality unchanged.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab5_data_pipeline_naming.py
```

---

# Step 2: Review a Poorly Named Data Script

Add the following code:

```python
d = [100, 200, 300]

r = []

for x in d:
    r.append(x * 1.1)

print(r)
```

### Questions

- What does d represent?
- What does r represent?
- What transformation is being applied?

The code works, but its purpose is unclear.

---

# Step 3: Run the Script

Execute:

```bash
python lab5_data_pipeline_naming.py
```

### Expected Output

```text
[110.0, 220.00000000000003, 330.0]
```

---

# Step 4: Refactor with Meaningful Names

Replace the code with:

```python
sales_amounts = [100, 200, 300]

adjusted_sales_amounts = []

for sales_amount in sales_amounts:
    adjusted_sales_amounts.append(sales_amount * 1.1)

print(adjusted_sales_amounts)
```

### Run Again

```bash
python lab5_data_pipeline_naming.py
```

### Observation

The output remains the same, but the code is much easier to understand.

---

# Step 5: Refactor a Data Cleaning Script

Review the following code:

```python
n = [" Alice ", " Bob ", " Charlie "]

c = []

for i in n:
    c.append(i.strip())

print(c)
```

### Task

Rename the variables.

### Suggested Solution

```python
customer_names = [" Alice ", " Bob ", " Charlie "]

clean_customer_names = []

for customer_name in customer_names:
    clean_customer_names.append(customer_name.strip())

print(clean_customer_names)
```

---

# Step 6: Refactor a Transformation Script

Review the following code:

```python
v = [1000, 2000, 3000]

o = []

for i in v:
    o.append(i * 0.9)

print(o)
```

### Your Task

Rename variables using meaningful business names.

### Example

```python
product_prices = [1000, 2000, 3000]

discounted_prices = []

for product_price in product_prices:
    discounted_prices.append(product_price * 0.9)

print(discounted_prices)
```

---

# Step 7: Create a Simple Data Pipeline

Add the following code:

```python
raw_sales_data = [100, 200, 300, 400]

clean_sales_data = []

for sales_amount in raw_sales_data:
    clean_sales_data.append(float(sales_amount))

tax_adjusted_sales = []

for sales_amount in clean_sales_data:
    tax_adjusted_sales.append(sales_amount * 1.18)

print("Raw Data:", raw_sales_data)
print("Clean Data:", clean_sales_data)
print("Tax Adjusted Data:", tax_adjusted_sales)
```

### Run the Program

```bash
python lab5_data_pipeline_naming.py
```

### Sample Output

```text
Raw Data: [100, 200, 300, 400]
Clean Data: [100.0, 200.0, 300.0, 400.0]
Tax Adjusted Data: [118.0, 236.0, 354.0, 472.0]
```

### Pipeline Stages

1. Raw Data
2. Clean Data
3. Transformed Data

Notice how the variable names clearly indicate each stage.

---

# Step 8: Compare Bad vs Good Naming

### Poor Naming

```python
d = [100, 200]
r = []
x = 0
```

### Better Naming

```python
sales_amounts = [100, 200]
adjusted_sales_amounts = []
sales_amount = 0
```

### Benefits

- Self-documenting code
- Easier onboarding of team members
- Easier debugging
- Easier maintenance
- Better code reviews

---

# Challenge Exercise

Refactor the following script:

```python
a = [50, 100, 150]

b = []

for c in a:
    b.append(c * 2)

print(b)
```

### Requirements

Use meaningful names that describe:

- The original data
- The transformed data
- The loop variable

Example domains:

- Sales
- Customers
- Inventory
- Product prices

---

# Knowledge Check

1. Why are descriptive variable names important in data pipelines?
2. What is wrong with variable names such as d, r, and x?
3. What naming convention does PEP 8 recommend?
4. How do meaningful names help during debugging?
5. Why should transformation stages be clearly identified?

---

# Summary

In this lab, you learned how to:

- Improve clarity in data-processing scripts
- Use descriptive variable names
- Apply PEP 8 naming conventions
- Identify stages of a data pipeline through naming
- Refactor transformation scripts for better readability

Clear naming is one of the simplest ways to improve the quality of data engineering, analytics, and ETL/ELT scripts.
