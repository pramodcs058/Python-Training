# Lab 2: Convert Between Numeral Systems Using Python Built-in Functions

## Lab Objective

In this lab, you will learn how to:

* Convert decimal numbers to binary using `bin()`
* Convert decimal numbers to octal using `oct()`
* Convert decimal numbers to hexadecimal using `hex()`
* Convert binary values to decimal using `int()`
* Convert octal values to decimal using `int()`
* Convert hexadecimal values to decimal using `int()`
* Perform conversions between multiple numeral systems

---

# Prerequisites

* Python 3.x installed
* Visual Studio Code (or any Python IDE)
* Basic understanding of variables and data types

---

# Understanding Numeral Systems

Computers use different numeral systems to represent data.

| Numeral System | Base | Example  |
| -------------- | ---- | -------- |
| Binary         | 2    | 1010     |
| Octal          | 8    | 12       |
| Decimal        | 10   | 10       |
| Hexadecimal    | 16   | A, F, 1A |

Python provides built-in functions to convert between these systems.

---

# Step 1: Create a New Python File

1. Open Visual Studio Code.
2. Open the **PythonLabs** folder.
3. Create a new file named:

```text
lab2_numeral_systems.py
```

---

# Step 2: Convert Decimal to Binary

Add the following code:

```python
decimal_number = 25

binary_number = bin(decimal_number)

print("Decimal:", decimal_number)
print("Binary:", binary_number)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Decimal: 25
Binary: 0b11001
```

### Notes

* `bin()` converts a decimal integer into a binary string.
* The prefix `0b` indicates a binary value.

---

# Step 3: Convert Decimal to Octal

Add the following code:

```python
decimal_number = 25

octal_number = oct(decimal_number)

print("Decimal:", decimal_number)
print("Octal:", octal_number)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Decimal: 25
Octal: 0o31
```

### Notes

* `oct()` converts a decimal integer into an octal string.
* The prefix `0o` indicates an octal value.

---

# Step 4: Convert Decimal to Hexadecimal

Add the following code:

```python
decimal_number = 255

hexadecimal_number = hex(decimal_number)

print("Decimal:", decimal_number)
print("Hexadecimal:", hexadecimal_number)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Decimal: 255
Hexadecimal: 0xff
```

### Notes

* `hex()` converts a decimal integer into a hexadecimal string.
* The prefix `0x` indicates a hexadecimal value.

---

# Step 5: Convert Binary to Decimal

Add the following code:

```python
binary_value = "11001"

decimal_value = int(binary_value, 2)

print("Binary:", binary_value)
print("Decimal:", decimal_value)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Binary: 11001
Decimal: 25
```

### Notes

* `int(value, 2)` converts a binary string into a decimal integer.
* The second argument specifies the base.

---

# Step 6: Convert Octal to Decimal

Add the following code:

```python
octal_value = "31"

decimal_value = int(octal_value, 8)

print("Octal:", octal_value)
print("Decimal:", decimal_value)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Octal: 31
Decimal: 25
```

### Notes

* `int(value, 8)` converts an octal string into a decimal integer.
* The second argument specifies the base.

---

# Step 7: Convert Hexadecimal to Decimal

Add the following code:

```python
hex_value = "FF"

decimal_value = int(hex_value, 16)

print("Hexadecimal:", hex_value)
print("Decimal:", decimal_value)
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Expected Output

```text
Hexadecimal: FF
Decimal: 255
```

### Notes

* `int(value, 16)` converts a hexadecimal string into a decimal integer.

---

# Step 8: Perform Multiple Conversions

Replace the code with the following:

```python
decimal_number = 100

binary_number = bin(decimal_number)
octal_number = oct(decimal_number)
hexadecimal_number = hex(decimal_number)

print("Decimal:", decimal_number)
print("Binary:", binary_number)
print("Octal:", octal_number)
print("Hexadecimal:", hexadecimal_number)

binary_input = "1010"
octal_input = "144"
hex_input = "1A"

print("Binary to Decimal:", int(binary_input, 2))
print("Octal to Decimal:", int(octal_input, 8))
print("Hexadecimal to Decimal:", int(hex_input, 16))
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Sample Output

```text
Decimal: 100
Binary: 0b1100100
Octal: 0o144
Hexadecimal: 0x64
Binary to Decimal: 10
Octal to Decimal: 100
Hexadecimal to Decimal: 26
```

---

# Step 9: User Input Conversion

Add the following code:

```python
decimal_number = int(
    input("Enter a decimal number: ")
)

print("Binary:", bin(decimal_number))
print("Octal:", oct(decimal_number))
print("Hexadecimal:", hex(decimal_number))
```

### Run the Program

```bash
python lab2_numeral_systems.py
```

### Sample Execution

```text
Enter a decimal number: 50

Binary: 0b110010
Octal: 0o62
Hexadecimal: 0x32
```

---

# Challenge Exercise

Create a program that:

1. Accepts a decimal number from the user.
2. Converts it to binary.
3. Converts it to octal.
4. Converts it to hexadecimal.
5. Displays all values.

### Example

```text
Input: 75

Decimal: 75
Binary: 0b1001011
Octal: 0o113
Hexadecimal: 0x4b
```

---

# Mini Project

Create a Number System Converter that:

1. Accepts a decimal number from the user.
2. Displays:

   * Binary value
   * Octal value
   * Hexadecimal value
3. Displays the conversion report in a structured format.

Example:

```text
------ Conversion Report ------

Decimal      : 150
Binary       : 0b10010110
Octal        : 0o226
Hexadecimal  : 0x96

------------------------------
```

---

# Knowledge Check

1. Which function converts a decimal number to binary?
2. Which function converts a decimal number to octal?
3. Which function converts a decimal number to hexadecimal?
4. What does `int("1010", 2)` return?
5. What does `int("31", 8)` return?
6. What does `int("FF", 16)` return?
7. What do the prefixes `0b`, `0o`, and `0x` represent?
8. Why are different numeral systems used in computing?

---

# Summary

In this lab, you learned how to:

* Convert decimal numbers to binary using `bin()`
* Convert decimal numbers to octal using `oct()`
* Convert decimal numbers to hexadecimal using `hex()`
* Convert binary strings to decimal using `int(value, 2)`
* Convert octal strings to decimal using `int(value, 8)`
* Convert hexadecimal strings to decimal using `int(value, 16)`
* Accept user input and perform numeral system conversions

These conversions are commonly used in programming, operating systems, networking, cybersecurity, embedded systems, and data processing applications.
