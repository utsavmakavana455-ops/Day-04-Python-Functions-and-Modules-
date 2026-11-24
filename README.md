# Day 04 – Python Functions and Modules 


## 🎯 Learning Objectives

- Understand Python functions.
- Create functions using `def`.
- Learn parameters and arguments.
- Understand return statements.
- Practice default arguments.
- Learn keyword arguments.
- Understand `*args` and `**kwargs`.
- Create lambda functions.
- Import and use Python modules.
- Create custom Python modules.

---

## 1. Python Functions

A function is a reusable block of code that performs a specific task.

```python
def greet():
    print("Hello! Welcome to Python")

greet()
```

## 2. Functions with Parameters

Parameters allow us to pass information into functions.

```python
def greet(name):
    print("Hello", name)

greet("Alex")
greet("John")
```

## 3. Multiple Parameters

```python
def student_info(name, age, country):
    print("Name:", name)
    print("Age:", age)
    print("Country:", country)

student_info("Alex", 22, "Germany")
```

## 4. Return Statements

The return statement sends a result back from a function.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

## 5. Default Arguments

```python
def greet(name="Student"):
    print("Hello", name)

greet()
greet("Alex")
```

## 6. Keyword Arguments

```python
def student(name, age):
    print(name, age)

student(age=22, name="Alex")
```

## 7. *args

Allows a function to receive multiple positional arguments.

```python
def calculate_sum(*numbers):
    return sum(numbers)

print(calculate_sum(10, 20))
print(calculate_sum(10, 20, 30, 40))
```

## 8. **kwargs

Allows a function to receive multiple keyword arguments.

```python
def student_details(**details):
    for key, value in details.items():
        print(key, ":", value)

student_details(
    name="Alex",
    age=22,
    country="Germany"
)
```

## 9. Lambda Functions

A lambda function is a small anonymous function.

```python
square = lambda x: x ** 2

print(square(5))
```

## 10. Python Modules

Modules allow us to reuse code from other Python files and libraries.

### Math Module

```python
import math

print(math.sqrt(25))
print(math.pi)
print(math.factorial(5))
```

### Random Module

```python
import random

number = random.randint(1, 100)

print(number)
```

### Import Specific Functions

```python
from math import sqrt

print(sqrt(64))
```

## 11. Creating Custom Modules

Create a file named `calculator.py`.

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Cannot divide by zero"
    return a / b
```

Create another file named `main.py`.

```python
import calculator

print(calculator.add(10, 20))
print(calculator.subtract(20, 5))
print(calculator.multiply(5, 4))
print(calculator.divide(20, 4))
```

## 12. Practical Machine Learning Example

Using functions to calculate student averages and results.

```python
def calculate_average(marks):
    return sum(marks) / len(marks)

def check_result(average):
    if average >= 50:
        return "Passed"
    return "Failed"

students = {
    "Alex": [80, 90, 85],
    "John": [40, 45, 50],
    "Sarah": [90, 95, 92]
}

for name, marks in students.items():
    average = calculate_average(marks)
    result = check_result(average)

    print(name, average, result)
```

## 13. Coding Exercises

- [ ] Create a function that prints your name.
- [ ] Create a function that adds two numbers.
- [ ] Create a function that checks even or odd.
- [ ] Calculate factorial using a function.
- [ ] Find the largest number in a list.
- [ ] Create a lambda function to calculate squares.
- [ ] Import math and calculate square root.
- [ ] Create a student function using `**kwargs`.

## 14. Key Concepts Summary

| Concept | Purpose |
|---|---|
| `def` | Define a function |
| `return` | Return a result |
| Parameters | Receive input |
| Default arguments | Provide default values |
| `*args` | Multiple positional arguments |
| `**kwargs` | Multiple keyword arguments |
| `lambda` | Create small anonymous functions |
| `import` | Import modules |

## 📚 Day 4 Summary

Today I learned:

- Python Functions
- Parameters and Arguments
- Return Statements
- Default and Keyword Arguments
- *args and **kwargs
- Lambda Functions
- Built-in Modules
- Custom Modules

## Why Is This Important for Machine Learning?

Functions help organize Machine Learning workflows into reusable components:

- Data cleaning
- Data preprocessing
- Feature engineering
- Model training
- Model evaluation


