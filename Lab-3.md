# Lab 3: Simulate Encoding and Decoding Using Numeral System Conversions

## Lab Objective

In this lab, you will learn how to:

- Use decimal, binary, and hexadecimal conversions from Lab 2
- Simulate simple data encoding and decoding processes
- Convert text characters into numeric representations
- Encode data into hexadecimal format
- Decode hexadecimal values back into readable text
- Understand how computers store and transmit data

---

# Prerequisites

Before starting this lab, you should know:

- Variables and data types
- String handling
- Python built-in functions:
  - bin()
  - hex()
  - int()
  - ord()
  - chr()

---

# Scenario

Computers do not store text directly. Instead, they store numeric values representing characters.

For example:

```text
A → 65
B → 66
C → 67
```

These values can be represented in:

- Decimal
- Binary
- Hexadecimal

In this lab, you will simulate a simple encoding and decoding process.

---

# Step 1: Create a New Python File

Create a file named:

```text
lab3_encoding_decoding.py
```

---

# Step 2: Convert a Character to Decimal

Add the following code:

```python
character = "A"

ascii_value = ord(character)

print("Character:", character)
print("Decimal Value:", ascii_value)
```

### Run the Program

```bash
python lab3_encoding_decoding.py
```

### Expected Output

```text
Character: A
Decimal Value: 65
```

### Notes

- `ord()` returns the numeric value of a character.

---

# Step 3: Convert Decimal to Binary and Hexadecimal

Add the following code:

```python
character = "A"

ascii_value = ord(character)

binary_value = bin(ascii_value)
hex_value = hex(ascii_value)

print("Character:", character)
print("Decimal:", ascii_value)
print("Binary:", binary_value)
print("Hexadecimal:", hex_value)
```

### Expected Output

```text
Character: A
Decimal: 65
Binary: 0b1000001
Hexadecimal: 0x41
```

### Notes

This process is similar to encoding data before storage or transmission.

---

# Step 4: Encode an Entire Word

Replace the code with:

```python
word = "DATA"

print("Original Word:", word)

for character in word:
    print(character, "=", hex(ord(character)))
```

### Run the Program

```bash
python lab3_encoding_decoding.py
```

### Sample Output

```text
Original Word: DATA
D = 0x44
A = 0x41
T = 0x54
A = 0x41
```

---

# Step 5: Create a Simple Encoder

Add the following code:

```python
message = "HELLO"

encoded_message = []

for character in message:
    encoded_message.append(hex(ord(character)))

print("Original Message:", message)
print("Encoded Message:", encoded_message)
```

### Sample Output

```text
Original Message: HELLO
Encoded Message:
['0x48', '0x45', '0x4c', '0x4c', '0x4f']
```

### Notes

This hexadecimal list represents the encoded form of the message.

---

# Step 6: Decode Hexadecimal Values Back to Text

Replace the code with:

```python
encoded_message = ['0x48', '0x45', '0x4c', '0x4c', '0x4f']

decoded_message = ""

for value in encoded_message:
    decimal_value = int(value, 16)
    decoded_message += chr(decimal_value)

print("Encoded Message:", encoded_message)
print("Decoded Message:", decoded_message)
```

### Expected Output

```text
Encoded Message:
['0x48', '0x45', '0x4c', '0x4c', '0x4f']

Decoded Message:
HELLO
```

### Notes

- `int(value, 16)` converts hexadecimal to decimal.
- `chr()` converts a decimal value back into a character.

---

# Step 7: Build a Complete Encode/Decode Program

Add the following code:

```python
message = input("Enter a message: ")

encoded_values = []

for character in message:
    encoded_values.append(hex(ord(character)))

print("\nEncoded Data:")
print(encoded_values)

decoded_message = ""

for value in encoded_values:
    decoded_message += chr(int(value, 16))

print("\nDecoded Message:")
print(decoded_message)
```

### Run the Program

```bash
python lab3_encoding_decoding.py
```

### Sample Execution

```text
Enter a message: PYTHON

Encoded Data:
['0x50', '0x59', '0x54', '0x48', '0x4f', '0x4e']

Decoded Message:
PYTHON
```

---

# Challenge Exercise

Enhance the program to display:

1. Character
2. Decimal value
3. Binary value
4. Hexadecimal value

Example:

```text
Character: A
Decimal: 65
Binary: 0b1000001
Hexadecimal: 0x41
```

Display this information for every character entered by the user.

---

# Real-World Connection

Many technologies use encoding and decoding:

- Network communication
- File storage
- APIs
- Databases
- Encryption systems
- Data serialization formats

Although real-world systems use more advanced techniques, the concept is based on converting information into numeric representations.

---

# Knowledge Check

1. What does the `ord()` function do?
2. What does the `chr()` function do?
3. Which function converts decimal to binary?
4. Which function converts decimal to hexadecimal?
5. How do you convert a hexadecimal string to decimal?
6. Why is encoding used in computer systems?

---

# Summary

In this lab, you learned how to:

- Convert characters to decimal values using `ord()`
- Convert decimal values to binary using `bin()`
- Convert decimal values to hexadecimal using `hex()`
- Convert hexadecimal values back to decimal using `int(value, 16)`
- Convert decimal values back to characters using `chr()`
- Simulate a simple encoding and decoding workflow similar to real-world data processing systems
