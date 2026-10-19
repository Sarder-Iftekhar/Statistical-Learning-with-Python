# 2.1 Variables in Python

## 📚 Contents

- [What Are Variables?](#1-what-are-variables)
- [Creating Variables](#2-creating-variables)
- [Variable Naming Rules](#3-variable-naming-rules)
- [Dynamic Typing](#4-dynamic-typing)
- [Displaying Variable Values](#5-displaying-variable-values)
- [Summary](#6-summary)
- [Practice Exercises](#7-practice-exercises)

---

## 1. What Are Variables?

Variables are used to store data in a program. They allow us to save values and use or modify them whenever needed.

In Python, a variable is created when you assign a value to a name using the assignment operator (`=`).

### Example

```python
my_variable = 4

print(my_variable)
```

**Output:**

```text
4
```

Here:
- `my_variable` is the variable name.
- `=` is the assignment operator.
- `4` is the value assigned to the variable.

---

## 2. Creating Variables

In Python, you do not need to declare a variable's data type explicitly. Simply assign a value to a variable, and Python determines its type at runtime.

### Examples

```python
# Integer
age = 20

# Float
height = 1.75

# String
name = "Alex"

# Boolean
is_student = True

print(age)
print(height)
print(name)
print(is_student)
```

**Output:**

```text
20
1.75
Alex
True
```

You can also assign a new value to an existing variable.

```python
my_variable = 4

my_variable = "Hello World"

print(my_variable)
```

**Output:**

```text
Hello World
```

The original value `4` is replaced by the string `"Hello World"`.

---

## 3. Variable Naming Rules

Python has specific rules for naming variables.

### Rule 1: Must Start with a Letter or Underscore

A variable name must begin with a letter (`A-Z`, `a-z`) or an underscore (`_`). It cannot start with a number.

```python
# Valid
name = "Alex"
_age = 20
student1 = "Sam"

# Invalid
# 1student = "Sam"
```

### Rule 2: Only Letters, Numbers, and Underscores

Variable names can contain letters, numbers, and underscores, but they cannot contain spaces or special characters such as `@` or `-`.

```python
# Valid
my_variable = 10
student_age = 21
score2 = 95

# Invalid
# my-variable = 10
# student age = 21
# score@ = 95
```

### Rule 3: Variable Names Are Case-Sensitive

Python treats uppercase and lowercase letters as different characters.

```python
my_variable = 10
my_Variable = 20
My_Variable = 30

print(my_variable)
print(my_Variable)
print(My_Variable)
```

**Output:**

```text
10
20
30
```

These are three separate variables.

### Rule 4: Use Descriptive Names

Choose names that clearly describe the data stored in the variable.

```python
# Less descriptive
x = 86

# More descriptive
num_neurons = 86
```

Descriptive names make your code easier to understand and maintain.

### Rule 5: Follow the snake_case Convention

In Python, it is common practice to use `snake_case` for variable names. Words are written in lowercase and separated by underscores.

```python
first_name = "Alex"
total_score = 95
number_of_students = 30
```

**Tip:** Avoid using Python keywords such as `if`, `for`, `class`, and `return` as variable names.

---

## 4. Dynamic Typing

Python is a **dynamically typed language**. This means that you do not need to specify a variable's type when creating it. Python determines the type of the value at runtime.

You can check a variable's current type using the built-in `type()` function.

### Example

```python
my_variable = 4
print(type(my_variable))

my_variable = "Hello World"
print(type(my_variable))
```

**Output:**

```text
<class 'int'>
<class 'str'>
```

Initially, `my_variable` refers to an integer. Later, it refers to a string.

This flexibility allows you to reuse variable names for different values, although using different names for conceptually different data often makes code easier to read.

---

## 5. Displaying Variable Values

The built-in `print()` function allows you to display the value of a variable.

### Example

```python
name = "Alex"
age = 20

print(name)
print(age)
```

**Output:**

```text
Alex
20
```

You can also display text and variable values together using an f-string.

```python
name = "Alex"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

**Output:**

```text
My name is Alex and I am 20 years old.
```

### Variables in Jupyter Notebooks

In interactive environments such as Jupyter Notebook, you can display the value of the last expression in a code cell without explicitly calling `print()`.

```python
my_variable = "Hello World"

my_variable
```

**Output:**

```text
'Hello World'
```

However, in regular Python scripts (`.py` files), use `print()` when you want to display a value.

---

## 6. Summary

Variables are essential building blocks of Python programs.

Key takeaways:

- Variables store values that can be used throughout a program.
- Use the assignment operator (`=`) to assign a value to a variable.
- Python determines the data type at runtime through dynamic typing.
- You can reassign a variable to a new value, including a value of a different type.
- Variable names must start with a letter or underscore.
- Variable names can contain letters, numbers, and underscores.
- Python variable names are case-sensitive.
- Use descriptive names and follow the `snake_case` naming convention.
- Use `print()` to display variable values.

---

## 7. Practice Exercises

Try solving these exercises on your own.

### Exercise 1: Create Variables

Create variables to store the following information:

- Your name
- Your age
- Your height
- Whether you are a student

Print all four variables.

### Exercise 2: Reassign a Variable

Create a variable named `my_variable` and assign it the value `100`. Then assign it the string `"Python"` and print the result.

### Exercise 3: Check Data Types

Create the following variables and use `type()` to identify their data types.

```python
age = 25
price = 19.99
language = "Python"
is_learning = True
```

### Exercise 4: Naming Variables

Identify which of the following are valid Python variable names:

```python
student_name = "Alex"
2nd_student = "Sam"
_total = 100
student-age = 20
score2 = 95
my variable = 10
```

### Exercise 5: Use an f-string

Create two variables, `name` and `age`, then print a sentence in this format:

```text
My name is Alex and I am 20 years old.
```

---

