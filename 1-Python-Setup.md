# Python Setup Guide for VS Code

This guide walks you through installing Python, setting up Visual Studio Code (VS Code), configuring the Python environment, and running Python programs successfully.

---

# Overview

By following this guide, you will learn how to:

* Install Python
* Verify the Python installation
* Install Visual Studio Code
* Install the Python Extension for VS Code
* Configure the Python Interpreter
* Run Python programs
* Debug Python applications

---

# Prerequisites

* Windows, macOS, or Linux operating system
* Internet connection
* Administrator privileges for software installation

---

# Step 1: Install Python

## Download Python

1. Open your web browser.
2. Navigate to the official Python website:

   * https://www.python.org/downloads/
3. Download the latest stable Python 3.x release.

## Install Python

1. Run the downloaded installer.

2. Before clicking **Install Now**, ensure the following option is selected:

   ```text
   Add Python to PATH
   ```

3. Click **Install Now**.

4. Wait for the installation to complete.

### Why Add Python to PATH?

Adding Python to PATH allows you to execute Python commands from any terminal or command prompt window.

---

## Verify Python Installation

### Windows

Open **Command Prompt** and run:

```bash
python --version
```

### macOS/Linux

Open **Terminal** and run:

```bash
python3 --version
```

### Sample Output

```text
Python 3.12.2
```

If a version number is displayed, Python has been installed successfully.

---

# Step 2: Install Visual Studio Code

## Download VS Code

1. Open your browser.

2. Navigate to:

   https://code.visualstudio.com

3. Download the installer for your operating system.

---

## Install VS Code

1. Run the installer.
2. Accept the default installation settings.
3. Complete the installation process.
4. Launch Visual Studio Code.

---

# Step 3: Install the Python Extension

The Python Extension adds support for:

* IntelliSense (Auto-completion)
* Syntax Highlighting
* Linting
* Debugging
* Jupyter Notebook Integration

---

## Install Extension

1. Open Visual Studio Code.

2. Select **Extensions** from the left sidebar.

   Or press:

   ```text
   Ctrl + Shift + X
   ```

3. Search for:

   ```text
   Python
   ```

4. Locate the extension published by **Microsoft**.

5. Click **Install**.

---

# Step 4: Configure the Python Interpreter

VS Code must know which Python installation to use.

## Select Interpreter

1. Open VS Code.

2. Create a new Python file or open an existing `.py` file.

3. Press:

   ```text
   Ctrl + Shift + P
   ```

4. Search for:

   ```text
   Python: Select Interpreter
   ```

5. Select the installed Python version.

Example:

```text
Python 3.12.x
```

6. VS Code will now use this interpreter for running and debugging Python programs.

---

# Step 5: Create Your First Python Program

Create a new file named:

```text
hello.py
```

Add the following code:

```python
print("Hello, World!")
```

Save the file.

---

# Step 6: Run Python Code

## Option A: Run from the Terminal

### Open Integrated Terminal

Press:

```text
Ctrl + `
```

Or navigate to:

```text
Terminal → New Terminal
```

### Execute the Program

Run:

```bash
python hello.py
```

### Expected Output

```text
Hello, World!
```

---

## Option B: Run Using the Play Button

1. Open the Python file.
2. Click the **Run ▶** button located in the upper-right corner.
3. VS Code executes the program automatically.

### Expected Output

```text
Hello, World!
```

The output will appear in the integrated terminal.

---

# Step 7: Debug Python Programs

Debugging helps identify and fix issues in your code.

---

## Add a Breakpoint

1. Open your Python file.
2. Click to the left of a line number.

A red dot appears:

```text
● Breakpoint
```

---

## Start Debugging

Press:

```text
F5
```

Or navigate to:

```text
Run → Start Debugging
```

---

## Debug Controls

When execution pauses at a breakpoint, use the toolbar:

| Action    | Shortcut    |
| --------- | ----------- |
| Continue  | F5          |
| Step Over | F10         |
| Step Into | F11         |
| Step Out  | Shift + F11 |
| Stop      | Shift + F5  |

---

# Step 8: Verify Your Environment

Create a file named:

```text
environment_test.py
```

Add:

```python
import sys

print("Python Version:")
print(sys.version)

print("\\nPython Executable:")
print(sys.executable)
```

Run:

```bash
python environment_test.py
```

### Sample Output

```text
Python Version:
3.12.2

Python Executable:
C:\\Python312\\python.exe
```

This confirms that VS Code is using the correct Python interpreter.

---

# Quick Reference

| Step                     | Action                 | Command / Shortcut |
| ------------------------ | ---------------------- | ------------------ |
| Install Python           | Verify installation    | `python --version` |
| Install VS Code          | Launch editor          | Open VS Code       |
| Install Python Extension | Extensions Marketplace | `Ctrl + Shift + X` |
| Select Interpreter       | Configure Python       | `Ctrl + Shift + P` |
| Open Terminal            | Run commands           | `Ctrl + ``         |
| Run Program              | Execute Python file    | `python file.py`   |
| Start Debugging          | Debug application      | `F5`               |

---

# Troubleshooting

## Python Command Not Found

### Windows

Verify Python is added to PATH:

```bash
python --version
```

If the command is not recognized:

1. Reinstall Python.
2. Ensure **Add Python to PATH** is checked.

---

## Interpreter Not Showing in VS Code

1. Restart VS Code.
2. Reinstall the Python Extension.
3. Use:

```text
Ctrl + Shift + P
```

and select:

```text
Python: Select Interpreter
```

---

## Program Does Not Run

Verify:

* Python is installed.
* The file extension is `.py`.
* The correct interpreter is selected.
* The file is saved before execution.

---

# Summary

You have successfully learned how to:

* Install Python
* Verify the installation
* Install Visual Studio Code
* Install the Python Extension
* Configure the Python Interpreter
* Create and run Python programs
* Debug Python applications
* Troubleshoot common setup issues

You are now ready to begin working through the Python lab exercises in this repository.
