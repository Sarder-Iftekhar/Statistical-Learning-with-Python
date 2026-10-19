# 2.2 Built-in Data Types in Python

Python provides several built-in data types that help us store, represent, and manipulate different kinds of information.

Understanding these data types is one of the first steps toward learning Python programming.

## 📚 Contents

- [Integers](#1-integers)
- [Floating-Point Numbers](#2-floating-point-numbers)
- [Strings](#3-strings)
- [Booleans](#4-booleans)
- [None](#5-none)
- [Checking Data Types](#6-checking-data-types)
- [Summary](#7-summary)

---

## 1. Integers

An **integer (`int`)** is a whole number without a decimal point. Integers can be positive, negative, or zero.

Examples: `10`, `20`, `0`, `-5`

### Example

```python
subjects_group_1 = 10
subjects_group_2 = 20
measurements_total = 60

subjects_total = subjects_group_1 + subjects_group_2

print(subjects_total)
```

**Output:**

```text
30
```

### Mathematical Operations

Python supports several arithmetic operations on integers.

```python
a = 10
b = 3

print(a + b)  # Addition: 13
print(a - b)  # Subtraction: 7
print(a * b)  # Multiplication: 30
print(a / b)  # Division: 3.333...
print(a // b) # Floor division: 3
print(a % b)  # Modulus: 1
print(a ** b) # Exponentiation: 1000
```

### Division Example

```python
measurements_per_subject = measurements_total / subjects_total

print(measurements_per_subject)
```

**Output:**

```text
2.0
```

Notice that `/` returns a floating-point number, even when both operands are integers.

**Note:** In Jupyter notebooks, you can display the value of the last expression in a cell without using `print()`. In regular Python scripts (`.py` files), use `print()` when you want to display a value.

---

## 2. Floating-Point Numbers

A **floating-point number (`float`)** represents a number that can contain a fractional or decimal part.

Examples: `3.14`, `2.0`, `-1.5`, `0.25`

### Example

```python
roughly_pi = 3.14
radius = 2

circumference = 2 * roughly_pi * radius

print("The circumference of the circle is", circumference)
```

**Output:**

```text
The circumference of the circle is 12.56
```

Python supports arithmetic operations on floating-point numbers, just as it does on integers.

```python
x = 5.5
y = 2.0

print(x + y)  # 7.5
print(x - y)  # 3.5
print(x * y)  # 11.0
print(x / y)  # 2.75
```

### Integers vs. Floats

```python
a = 10
b = 10.0

print(type(a))  # <class 'int'>
print(type(b))  # <class 'float'>
```

Although `10` and `10.0` represent the same mathematical value, Python stores them as different data types.

**Important:** Floating-point numbers are approximations for many decimal values. Therefore, some calculations may produce results such as `0.30000000000000004` instead of exactly `0.3`.

---

## 3. Strings

A **string (`str`)** is a sequence of characters used to represent text.

Strings can contain letters, numbers, spaces, and special characters.

Examples: `"Hello"`, `'Python'`, `"psy111"`

### Creating Strings

Python allows both single and double quotation marks. The opening and closing quotation marks must match.

```python
module = "psy111"
university = 'Oldenburg'

print(module)
print(university)
```

**Output:**

```text
psy111
Oldenburg
```

### Common String Operations

**1. Finding the length**

The built-in `len()` function returns the number of characters in a string.

```python
module = "psy111"

print(len(module))
```

Output:

```text
6
```

**2. Converting to lowercase**

The `.lower()` method converts all letters in a string to lowercase.

```python
university = "Oldenburg"

print(university.lower())
```

Output:

```text
oldenburg
```

**3. Replacing part of a string**

The `.replace()` method replaces one substring with another.

```python
university = "Oldenburg"

print(university.replace("burg", "castle"))
```

Output:

```text
Oldencastle
```

Notice that `.replace()` returns a new string; it does not modify the original string in place.

### Formatted Strings (f-strings)

An **f-string** allows you to insert variables and expressions directly into a string.

Place the letter `f` before the opening quotation mark and enclose variables in curly brackets `{}`.

```python
num_neurons = 86

print(f"The human brain has {num_neurons} billion neurons.")
```

Output:

```text
The human brain has 86 billion neurons.
```

You can also format decimal numbers.

```python
pi = 3.14159265

print(f"Pi rounded to two decimal places is {pi:.2f}")
```

Output:

```text
Pi rounded to two decimal places is 3.14
```

**Tip:** Use f-strings when you want to combine text and variable values in a readable way.

---

## 4. Booleans

A **Boolean (`bool`)** represents a logical value. In Python, there are only two Boolean values:

- `True`
- `False`

These values are useful for comparisons, conditions, and logical operations.

**Important:** Python is case-sensitive. `True` and `False` are valid Boolean values, whereas `true` and `false` are not.

### Example

```python
i_like_psy111 = True

print(i_like_psy111)
print(type(i_like_psy111))
```

Output:

```text
True
<class 'bool'>
```

### Comparison Operators

Comparison operators compare values and return a Boolean result.

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `==` | Equal to | `5 == 3` | `False` |
| `!=` | Not equal to | `5 != 3` | `True` |
| `>` | Greater than | `5 > 3` | `True` |
| `<` | Less than | `5 < 3` | `False` |
| `>=` | Greater than or equal to | `5 >= 5` | `True` |
| `<=` | Less than or equal to | `3 <= 5` | `True` |

Example:

```python
print(5 > 3)
print(5 == 3)
print(10 != 5)
```

Output:

```text
True
False
True
```

### Logical Operators

Python provides three main logical operators:

- `and` — returns `True` when both conditions are true.
- `or` — returns `True` when at least one condition is true.
- `not` — reverses a Boolean value.

**Using `and`**

All conditions must be true.

```python
result = ("burg" in "oldenburg") and (5 > 3) and (4 * 2 == 8)

print(result)
```

Output:

```text
True
```

**Using `or`**

At least one condition must be true.

```python
result = ("burg" in "oldenburg") and (5 > 3) or (4 * 2 == 10)

print(result)
```

Output:

```text
True
```

The final comparison, `4 * 2 == 10`, is `False`. However, the expression before `or` is `True`, so the overall result is `True`.

**Using `not`**

```python
print(not True)
print(not False)
```

Output:

```text
False
True
```

**Tip:** Use parentheses to make complex logical expressions easier to read and understand.

---

## 5. None

`None` is a special built-in constant in Python that represents the absence of a value.

Its data type is `NoneType`.

### Example

```python
result = None

print(result)
print(type(result))
```

Output:

```text
None
<class 'NoneType'>
```

`None` is useful when a variable has no meaningful value yet, or when a function does not explicitly return a value.

### None vs. False

Although both can represent the absence of a useful result in different contexts, `None` and `False` are not the same.

```python
print(None == False)
print(None is None)
print(False is False)
```

Output:

```text
False
True
True
```

Use `is None` when checking whether a value is `None`.

```python
result = None

if result is None:
    print("No result available.")
```

Output:

```text
No result available.
```

**Note:** `None` is conceptually different from `0`, an empty string (`""`), and `False`.

---

## 6. Checking Data Types

Python provides the built-in `type()` function to identify the type of a value.

```python
age = 20
height = 1.75
name = "Alex"
is_student = True
result = None

print(type(age))
print(type(height))
print(type(name))
print(type(is_student))
print(type(result))
```

Output:

```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
<class 'NoneType'>
```

You can also use `isinstance()` to check whether a value belongs to a particular type.

```python
age = 20

print(isinstance(age, int))
print(isinstance(age, str))
```

Output:

```text
True
False
```

---

## 7. Summary

Python has several built-in data types that are essential for everyday programming.

| Data Type | Python Name | Example | Description |
|---|---|---|---|
| Integer | `int` | `10`, `-5`, `0` | Whole numbers |
| Floating-point | `float` | `3.14`, `2.0` | Numbers with fractional parts |
| String | `str` | `"Hello"` | Text and sequences of characters |
| Boolean | `bool` | `True`, `False` | Logical values |
| None | `NoneType` | `None` | Represents the absence of a value |

### Key Takeaways

- Use `int` for whole numbers.
- Use `float` for numbers with decimal or fractional parts.
- Use `str` for text.
- Use `bool` for logical values and comparison results.
- Use `None` to represent the absence of a value.
- Use `type()` to inspect an object's data type.
- Use `print()` to display results in regular Python scripts.
- Remember that Python is case-sensitive.

---

## 🧠 Practice Exercises

Try solving these exercises without looking at the solutions first.

**Exercise 1:** Identify the data type of each variable.

```python
a = 42
b = 3.14
c = "Python"
d = False
e = None

# Use type() to inspect each variable.
```

**Exercise 2:** Predict the output.

```python
x = 10
y = 3

print(x + y)
print(x / y)
print(x // y)
print(x % y)
print(x > y)
```

**Exercise 3:** Work with strings.

```python
university = "Oldenburg"

# Print the length of the string.
# Convert it to lowercase.
# Replace "burg" with "castle".
```

**Exercise 4:** Evaluate the logical expressions.

```python
print(5 > 3 and 10 < 20)
print(5 < 3 or 10 == 10)
print(not (4 == 4))
```

**Exercise 5:** Create an f-string.

```python
name = "Alex"
age = 20

# Print: My name is Alex and I am 20 years old.
```

---

**Next topic:** Type conversion and working with different data types in Python.
