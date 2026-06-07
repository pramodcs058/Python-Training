# Lab 7: Format Output Using print() with sep= and end= to Simulate Clean Data Logging

## Lab Objective

In this lab, you will learn how to:

- Use the `print()` function effectively
- Customize output using the `sep=` parameter
- Control line endings using the `end=` parameter
- Create readable log-style output
- Simulate simple data pipeline and ETL logging messages
- Improve the readability of console-based reports

---

# Prerequisites

Before starting this lab, you should know:

- Variables and data types
- The `print()` function
- Basic Python scripts

---

# Why Output Formatting Matters

In data engineering and analytics projects, logs are used to track:

- Data ingestion
- Data transformation
- Validation results
- Pipeline execution status
- Error messages

Poorly formatted logs are difficult to read.

Well-formatted logs help developers quickly understand what happened during execution.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab7_data_logging.py
```

---

# Step 2: Understand Default print() Behavior

Add the following code:

```python
employee_name = "Alice"
department = "Sales"
salary = 55000

print(employee_name, department, salary)
```

### Run the Program

```bash
python lab7_data_logging.py
```

### Expected Output

```text
Alice Sales 55000
```

### Observation

By default, `print()` separates values with a space.

---

# Step 3: Use the sep= Parameter

Replace the code with:

```python
employee_name = "Alice"
department = "Sales"
salary = 55000

print(employee_name,
      department,
      salary,
      sep=" | ")
```

### Run the Program

```bash
python lab7_data_logging.py
```

### Expected Output

```text
Alice | Sales | 55000
```

### Notes

The `sep=` parameter changes the separator between values.

---

# Step 4: Simulate a Data Log Entry

Add the following code:

```python
record_id = 101
status = "SUCCESS"
rows_processed = 250

print("Record ID",
      record_id,
      status,
      rows_processed,
      sep=" : ")
```

### Expected Output

```text
Record ID : 101 : SUCCESS : 250
```

This resembles a simple log message.

---

# Step 5: Create Structured Log Messages

Add the following code:

```python
pipeline_name = "Sales Pipeline"
stage = "Transformation"
status = "Completed"

print("[INFO]",
      pipeline_name,
      stage,
      status,
      sep=" | ")
```

### Expected Output

```text
[INFO] | Sales Pipeline | Transformation | Completed
```

---

# Step 6: Use the end= Parameter

Add the following code:

```python
print("Loading Data...", end=" ")
print("Completed")
```

### Expected Output

```text
Loading Data... Completed
```

### Notes

Normally, `print()` moves to a new line.

The `end=` parameter changes what is printed at the end.

Default:

```python
end="\n"
```

---

# Step 7: Simulate Pipeline Progress Updates

Replace the code with:

```python
print("[INFO] Extracting Data...", end=" ")
print("Done")

print("[INFO] Cleaning Data...", end=" ")
print("Done")

print("[INFO] Transforming Data...", end=" ")
print("Done")

print("[INFO] Loading Data...", end=" ")
print("Done")
```

### Run the Program

```bash
python lab7_data_logging.py
```

### Expected Output

```text
[INFO] Extracting Data... Done
[INFO] Cleaning Data... Done
[INFO] Transforming Data... Done
[INFO] Loading Data... Done
```

---

# Step 8: Create a Mini Data Processing Log

Add the following code:

```python
dataset_name = "Customer Data"
rows_read = 1000
rows_processed = 975
status = "SUCCESS"

print("Dataset",
      dataset_name,
      sep=" : ")

print("Rows Read",
      rows_read,
      sep=" : ")

print("Rows Processed",
      rows_processed,
      sep=" : ")

print("Status",
      status,
      sep=" : ")
```

### Sample Output

```text
Dataset : Customer Data
Rows Read : 1000
Rows Processed : 975
Status : SUCCESS
```

---

# Step 9: Build a Simple Logging Report

Add the following code:

```python
pipeline_name = "Sales ETL Pipeline"
records_loaded = 500
records_failed = 5

print("=" * 40)

print("PIPELINE",
      pipeline_name,
      sep=" : ")

print("RECORDS LOADED",
      records_loaded,
      sep=" : ")

print("RECORDS FAILED",
      records_failed,
      sep=" : ")

print("=" * 40)
```

### Sample Output

```text
========================================
PIPELINE : Sales ETL Pipeline
RECORDS LOADED : 500
RECORDS FAILED : 5
========================================
```

---

# Challenge Exercise

Create a logging report that displays:

- Job Name
- Execution Date
- Records Processed
- Records Rejected
- Job Status

Use:

```python
sep=" : "
```

and

```python
end=" "
```

where appropriate.

Example:

```text
JOB NAME : Customer ETL
EXECUTION DATE : 2026-01-01
RECORDS PROCESSED : 5000
RECORDS REJECTED : 25
JOB STATUS : SUCCESS
```

---

# Knowledge Check

1. What is the purpose of the `sep=` parameter?
2. What is the default separator used by `print()`?
3. What is the purpose of the `end=` parameter?
4. What is the default value of `end=`?
5. Why is formatting important in data logging?

---

# Summary

In this lab, you learned how to:

- Format output using `print()`
- Customize separators with `sep=`
- Control line endings with `end=`
- Simulate clean logging messages
- Create readable pipeline execution reports
- Improve console output for data engineering and analytics workflows

These techniques are commonly used in ETL pipelines, automation scripts, monitoring tools, and command-line applications.
