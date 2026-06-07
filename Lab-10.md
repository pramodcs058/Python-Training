# Lab 10: Build a Unit Converter with Structured CSV and JSON Logging

## Lab Objective

In this lab, you will learn how to:

- Accept structured user input
- Perform unit conversions using arithmetic operations
- Convert temperatures and distances
- Generate structured output suitable for CSV logging
- Generate structured output suitable for JSON logging
- Build a reusable unit conversion application

---

# Prerequisites

Before starting this lab, you should know:

- Variables and data types
- User input using `input()`
- Type casting with `float()`
- Conditional statements (`if`, `elif`, `else`)
- String formatting

---

# Scenario

Many data engineering and analytics applications collect measurements from users and systems.

Examples:

- Temperature sensors
- Distance tracking systems
- Inventory systems
- IoT devices
- Data pipelines

The collected data is often stored in:

- CSV format
- JSON format

In this lab, you will create a simple unit converter and generate structured output suitable for logging.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab10_unit_converter.py
```

---

# Step 2: Build a Celsius to Fahrenheit Converter

Add the following code:

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
python lab10_unit_converter.py
```

### Sample Output

```text
Enter temperature in Celsius: 25

Temperature in Fahrenheit: 77.0
```

---

# Step 3: Build a Meters to Kilometers Converter

Replace the code with:

```python
distance_meters = float(
    input("Enter distance in meters: ")
)

distance_kilometers = (
    distance_meters / 1000
)

print("Distance in Kilometers:",
      distance_kilometers)
```

### Sample Output

```text
Enter distance in meters: 2500

Distance in Kilometers: 2.5
```

---

# Step 4: Accept Conversion Type

Replace the code with:

```python
conversion_type = input(
    "Choose conversion "
    "(temperature/distance): "
).lower()

print("Selected:", conversion_type)
```

### Sample Output

```text
Choose conversion (temperature/distance): temperature

Selected: temperature
```

---

# Step 5: Add Conversion Logic

Replace the code with:

```python
conversion_type = input(
    "Choose conversion "
    "(temperature/distance): "
).lower()

if conversion_type == "temperature":

    celsius = float(
        input("Enter Celsius value: ")
    )

    result = (celsius * 9 / 5) + 32

    print("Fahrenheit:", result)

elif conversion_type == "distance":

    meters = float(
        input("Enter meters value: ")
    )

    result = meters / 1000

    print("Kilometers:", result)

else:
    print("Invalid conversion type")
```

### Test Both Conversions

Temperature:

```text
temperature
25
```

Distance:

```text
distance
5000
```

---

# Step 6: Create CSV-Style Output

Modify the code to display structured CSV output.

Example:

```python
conversion_type = "temperature"
input_value = 25
output_value = 77

print(
    "conversion_type,input_value,output_value"
)

print(
    conversion_type,
    input_value,
    output_value,
    sep=","
)
```

### Expected Output

```text
conversion_type,input_value,output_value
temperature,25,77
```

### Why CSV?

CSV is commonly used for:

- Data exports
- ETL pipelines
- Reporting systems
- Data ingestion processes

---

# Step 7: Create JSON-Style Output

Add the following code:

```python
conversion_type = "temperature"
input_value = 25
output_value = 77

print("{")
print(f'  "conversion_type": "{conversion_type}",')
print(f'  "input_value": {input_value},')
print(f'  "output_value": {output_value}')
print("}")
```

### Expected Output

```json
{
  "conversion_type": "temperature",
  "input_value": 25,
  "output_value": 77
}
```

### Why JSON?

JSON is commonly used for:

- APIs
- Event streaming
- Cloud applications
- Data exchange systems

---

# Step 8: Build a Complete Unit Converter

Replace the code with:

```python
conversion_type = input(
    "Choose conversion "
    "(temperature/distance): "
).lower()

if conversion_type == "temperature":

    input_value = float(
        input("Enter Celsius value: ")
    )

    output_value = (
        input_value * 9 / 5
    ) + 32

    target_unit = "Fahrenheit"

elif conversion_type == "distance":

    input_value = float(
        input("Enter Meters value: ")
    )

    output_value = (
        input_value / 1000
    )

    target_unit = "Kilometers"

else:

    print("Invalid conversion type")
    exit()

print("\n--- Conversion Result ---")

print("Conversion Type:",
      conversion_type)

print("Input Value:",
      input_value)

print("Output Value:",
      output_value)

print("Target Unit:",
      target_unit)
```

---

# Step 9: Generate CSV Log Output

Add the following code after the conversion:

```python
print("\nCSV Log")

print(
    "conversion_type,input_value,output_value,target_unit"
)

print(
    conversion_type,
    input_value,
    output_value,
    target_unit,
    sep=","
)
```

### Sample Output

```text
CSV Log

conversion_type,input_value,output_value,target_unit
temperature,25.0,77.0,Fahrenheit
```

---

# Step 10: Generate JSON Log Output

Add the following code:

```python
print("\nJSON Log")

print("{")
print(
    f'  "conversion_type": "{conversion_type}",'
)
print(
    f'  "input_value": {input_value},'
)
print(
    f'  "output_value": {output_value},'
)
print(
    f'  "target_unit": "{target_unit}"'
)
print("}")
```

### Sample Output

```json
{
  "conversion_type": "distance",
  "input_value": 5000,
  "output_value": 5,
  "target_unit": "Kilometers"
}
```

---

# Challenge Exercise

Enhance the converter to support:

1. Celsius → Fahrenheit
2. Fahrenheit → Celsius
3. Meters → Kilometers
4. Kilometers → Meters

Requirements:

- Validate user input
- Generate CSV output
- Generate JSON output
- Display a user-friendly summary report

---

# Real-World Applications

This type of solution is commonly used in:

- Data Engineering pipelines
- ETL/ELT workflows
- IoT telemetry systems
- API integrations
- Monitoring platforms
- Sensor data processing applications

---

# Knowledge Check

1. Why do we convert user input using `float()`?
2. What arithmetic formula converts Celsius to Fahrenheit?
3. What arithmetic formula converts meters to kilometers?
4. Why is CSV commonly used in data pipelines?
5. Why is JSON commonly used in APIs?
6. What are the benefits of structured logging?

---

# Summary

In this lab, you learned how to:

- Accept structured user input
- Perform arithmetic unit conversions
- Use conditional logic to support multiple conversions
- Create CSV-style output
- Create JSON-style output
- Build structured logs suitable for data engineering workflows

These techniques are frequently used in ETL pipelines, APIs, cloud applications, monitoring systems, and data processing platforms.
