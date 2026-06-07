# Lab 6: Prompt Users for Structured Input (Temperature, Distance, Currency, and More)

## Lab Objective

In this lab, you will learn how to:

- Collect structured input from users using `input()`
- Convert user input into numeric data types
- Process temperature, distance, and currency values
- Display formatted output
- Build simple interactive Python programs

---

# Prerequisites

Before starting this lab, you should know:

- Variables
- Data types (`int`, `float`, `str`)
- Using the `print()` function
- Basic arithmetic operations

---

# What is Structured Input?

Structured input is data collected in a predefined format.

Examples:

| Type | Example |
|--------|---------|
| Temperature | 25.5 °C |
| Distance | 15.2 km |
| Currency | 5000 INR |
| Weight | 72.5 kg |

Structured input allows programs to process information accurately.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab6_structured_input.py
```

---

# Step 2: Accept a Temperature Value

Add the following code:

```python
temperature_celsius = float(
    input("Enter temperature in Celsius: ")
)

print("Temperature:", temperature_celsius, "°C")
```

### Run the Program

```bash
python lab6_structured_input.py
```

### Sample Execution

```text
Enter temperature in Celsius: 30

Temperature: 30.0 °C
```

### Notes

- `input()` always returns text.
- `float()` converts text into a decimal number.

---

# Step 3: Convert Celsius to Fahrenheit

Replace the code with:

```python
temperature_celsius = float(
    input("Enter temperature in Celsius: ")
)

temperature_fahrenheit = (
    temperature_celsius * 9 / 5
) + 32

print("Temperature in Fahrenheit:",
      temperature_fahrenheit)
```

### Run the Program

```bash
python lab6_structured_input.py
```

### Sample Output

```text
Enter temperature in Celsius: 25

Temperature in Fahrenheit: 77.0
```

---

# Step 4: Accept a Distance Value

Add the following code:

```python
distance_km = float(
    input("Enter distance in kilometers: ")
)

distance_miles = distance_km * 0.621371

print("Distance in Miles:",
      distance_miles)
```

### Run the Program

```bash
python lab6_structured_input.py
```

### Sample Output

```text
Enter distance in kilometers: 10

Distance in Miles: 6.21371
```

---

# Step 5: Accept a Currency Amount

Add the following code:

```python
amount_inr = float(
    input("Enter amount in INR: ")
)

exchange_rate = 0.012

amount_usd = amount_inr * exchange_rate

print("Amount in USD:",
      amount_usd)
```

### Run the Program

```bash
python lab6_structured_input.py
```

### Sample Output

```text
Enter amount in INR: 5000

Amount in USD: 60.0
```

### Note

For simplicity, this lab uses a fixed exchange rate.

---

# Step 6: Accept Multiple Structured Inputs

Replace the code with:

```python
customer_name = input(
    "Enter customer name: "
)

purchase_amount = float(
    input("Enter purchase amount: ")
)

tax_rate = float(
    input("Enter tax percentage: ")
)

total_amount = (
    purchase_amount +
    (purchase_amount * tax_rate / 100)
)

print("\nCustomer:", customer_name)
print("Purchase Amount:", purchase_amount)
print("Total Amount:", total_amount)
```

### Sample Execution

```text
Enter customer name: Rahul
Enter purchase amount: 1000
Enter tax percentage: 18

Customer: Rahul
Purchase Amount: 1000.0
Total Amount: 1180.0
```

---

# Step 7: Build a Mini Conversion Utility

Add the following code:

```python
temperature_celsius = float(
    input("Enter temperature (°C): ")
)

distance_km = float(
    input("Enter distance (km): ")
)

amount_inr = float(
    input("Enter amount (INR): ")
)

temperature_fahrenheit = (
    temperature_celsius * 9 / 5
) + 32

distance_miles = (
    distance_km * 0.621371
)

amount_usd = amount_inr * 0.012

print("\n--- Conversion Results ---")
print("Fahrenheit:", temperature_fahrenheit)
print("Miles:", distance_miles)
print("USD:", amount_usd)
```

### Run the Program

```bash
python lab6_structured_input.py
```

### Sample Output

```text
Enter temperature (°C): 25
Enter distance (km): 10
Enter amount (INR): 5000

--- Conversion Results ---
Fahrenheit: 77.0
Miles: 6.21371
USD: 60.0
```

---

# Step 8: Format Output for Better Readability

Update the print statements:

```python
print(f"Fahrenheit: {temperature_fahrenheit:.2f}")
print(f"Miles: {distance_miles:.2f}")
print(f"USD: {amount_usd:.2f}")
```

### Sample Output

```text
Fahrenheit: 77.00
Miles: 6.21
USD: 60.00
```

---

# Challenge Exercise

Create a program that collects:

1. Employee Name
2. Hours Worked
3. Hourly Rate

Calculate:

```text
Total Salary = Hours Worked × Hourly Rate
```

Display all details clearly.

Example:

```text
Employee: Priya
Hours Worked: 40
Hourly Rate: 500
Total Salary: 20000
```

---

# Knowledge Check

1. What does the `input()` function return?
2. Why do we use `float()` with numeric input?
3. How do you convert Celsius to Fahrenheit?
4. Why is structured input important?
5. How can formatted strings improve output readability?

---

# Summary

In this lab, you learned how to:

- Collect structured user input
- Convert text input into numeric values
- Process temperature, distance, and currency data
- Perform calculations using user-provided values
- Format output for better readability
- Build simple interactive data-processing programs

Structured input is commonly used in business applications, data analytics, ETL workflows, web applications, and automation scripts.
