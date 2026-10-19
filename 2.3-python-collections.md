# 2.3 Collections in Python

## 📚 Contents

- [Introduction](#1-introduction)
- [Lists](#2-lists)
- [Indexing](#3-indexing)
- [Slicing](#4-slicing)
- [Modifying Lists](#5-modifying-lists)
- [Tuples](#6-tuples)
- [Dictionaries](#7-dictionaries)
- [Lists vs. Tuples vs. Dictionaries](#8-lists-vs-tuples-vs-dictionaries)
- [Summary](#9-summary)
- [Practice Exercises](#10-practice-exercises)

---

## 1. Introduction

Variables are useful for storing individual values, such as integers, floating-point numbers, and strings. However, many programming tasks require us to store multiple values in a single data structure.

Python provides several built-in collection types for this purpose. The three important collection types are:

- **Lists (`list`)** — ordered and mutable collections.
- **Tuples (`tuple`)** — ordered and immutable collections.
- **Dictionaries (`dict`)** — collections that store key-value pairs.

Collections make it easier to organize, access, and manipulate multiple values within a program.

---

## 2. Lists

A **list** is an ordered and mutable collection of elements.

Lists can contain different data types, including integers, floats, strings, Booleans, and even other collections.

Lists are created using square brackets `[]`, with individual elements separated by commas.

### Creating Lists

```python
# An empty list
empty_list = []

# A list containing different data types
random_stuff = ["apple", 3.14, True, 4]

# A list containing integers
numbers = [10, 20, 30, 40, 50]

print(random_stuff)
print(numbers)
```

**Output:**

```text
['apple', 3.14, True, 4]
[10, 20, 30, 40, 50]
```

### Important Characteristics of Lists

- Lists preserve the order of their elements.
- Lists allow duplicate values.
- Lists can contain elements of different data types.
- Lists are mutable, meaning their contents can be changed after creation.

Example:

```python
fruits = ["apple", "banana", "apple"]

print(fruits)
```

**Output:**

```text
['apple', 'banana', 'apple']
```

---

## 3. Indexing

**Indexing** allows us to access individual elements of a collection by their position.

Python uses **zero-based indexing**, which means the first element has index `0`, the second has index `1`, and so on.

### Example

```python
random_stuff = ["apple", 3.14, True, 4]

print(random_stuff[0])
print(random_stuff[1])
print(random_stuff[2])
print(random_stuff[3])
```

**Output:**

```text
apple
3.14
True
4
```

### Understanding Zero-Based Indexing

For a list containing four elements:

| Element | Positive Index | Negative Index |
|---|---:|---:|
| `"apple"` | `0` | `-4` |
| `3.14` | `1` | `-3` |
| `True` | `2` | `-2` |
| `4` | `3` | `-1` |

### Negative Indexing

Python also supports negative indexing. The index `-1` refers to the last element, `-2` refers to the second-to-last element, and so on.

```python
fruits = ["apple", "banana", "cherry", "orange"]

print(fruits[-1])
print(fruits[-2])
```

**Output:**

```text
orange
cherry
```

**Note:** Accessing an index outside the valid range raises an `IndexError`.

```python
fruits = ["apple", "banana", "cherry"]

# print(fruits[5])  # IndexError
```

---

## 4. Slicing

**Slicing** allows us to retrieve a portion of a list.

The general syntax is:

```python
list_name[start:stop:step]
```

- `start` — the index where slicing begins; included in the result.
- `stop` — the index where slicing ends; excluded from the result.
- `step` — the interval between selected elements.

### Basic Slicing

```python
random_stuff = ["apple", 3.14, True, 4]

print(random_stuff[1:3])
```

**Output:**

```text
[3.14, True]
```

The slice starts at index `1` and stops before index `3`. Therefore, it includes the elements at indices `1` and `2`, but not index `3`.

### More Slicing Examples

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[1:4])
print(numbers[:3])
print(numbers[3:])
print(numbers[:])
print(numbers[::2])
print(numbers[::-1])
```

**Output:**

```text
[20, 30, 40]
[10, 20, 30]
[40, 50, 60]
[10, 20, 30, 40, 50, 60]
[10, 30, 50]
[60, 50, 40, 30, 20, 10]
```

### Key Takeaways

- `numbers[1:4]` selects elements from index `1` up to, but not including, index `4`.
- `numbers[:3]` selects the first three elements.
- `numbers[3:]` selects elements from index `3` to the end.
- `numbers[::2]` selects every second element.
- `numbers[::-1]` returns a reversed copy of the list.

---

## 5. Modifying Lists

Lists are **mutable**, which means you can change their contents after they have been created.

### 5.1 Replacing an Element

You can modify an element by assigning a new value to its index.

```python
random_stuff = ["apple", 3.14, True, 4]

print("Before reassignment:", random_stuff)

random_stuff[0] = "banana"

print("After reassignment:", random_stuff)
```

**Output:**

```text
Before reassignment: ['apple', 3.14, True, 4]
After reassignment: ['banana', 3.14, True, 4]
```

### 5.2 Adding Elements with `append()`

The `.append()` method adds one element to the end of a list.

```python
fruits = ["apple", "banana"]

fruits.append("orange")

print(fruits)
```

**Output:**

```text
['apple', 'banana', 'orange']
```

### 5.3 Adding Multiple Elements with `extend()`

The `.extend()` method adds elements from another iterable to the end of a list.

```python
numbers = [1, 2, 3]

numbers.extend([4, 5])

print(numbers)
```

**Output:**

```text
[1, 2, 3, 4, 5]
```

### 5.4 Removing Elements with `remove()`

The `.remove()` method removes the first matching value from a list.

```python
fruits = ["apple", "banana", "orange"]

fruits.remove("banana")

print(fruits)
```

**Output:**

```text
['apple', 'orange']
```

### 5.5 Removing Elements with `pop()`

The `.pop()` method removes and returns an element. If no index is specified, it removes the last element.

```python
numbers = [10, 20, 30, 40]

removed_item = numbers.pop()

print("Removed item:", removed_item)
print("Updated list:", numbers)
```

**Output:**

```text
Removed item: 40
Updated list: [10, 20, 30]
```

### 5.6 Sorting a List

The `.sort()` method sorts a list in place.

```python
numbers = [5, 2, 8, 1, 3]

numbers.sort()

print(numbers)
```

**Output:**

```text
[1, 2, 3, 5, 8]
```

To sort in descending order:

```python
numbers.sort(reverse=True)

print(numbers)
```

**Output:**

```text
[8, 5, 3, 2, 1]
```

**Tip:** `.sort()` modifies the original list. The built-in `sorted()` function instead returns a new sorted list.

---

## 6. Tuples

A **tuple** is an ordered collection of elements that is immutable.

Tuples are similar to lists, but their elements cannot be reassigned, added, or removed after the tuple has been created.

Tuples are usually created using parentheses `()`.

### Creating Tuples

```python
my_tuple = ("Hello", 1, 2, 3, 4, 2, "Goodbye")

print(my_tuple)
```

**Output:**

```text
('Hello', 1, 2, 3, 4, 2, 'Goodbye')
```

Tuples can contain multiple data types and duplicate values.

### Accessing Tuple Elements

Like lists, tuples support indexing and slicing.

```python
my_tuple = ("Hello", 1, 2, 3, 4, 2, "Goodbye")

print(my_tuple[0])
print(my_tuple[2])
print(my_tuple[-1])
print(my_tuple[1:4])
```

**Output:**

```text
Hello
2
Goodbye
(1, 2, 3)
```

### Tuple Methods

Tuples have two commonly used built-in methods: `.count()` and `.index()`.

**Using `index()`**

The `.index()` method returns the index of the first occurrence of a specified value.

```python
my_tuple = ("Hello", 1, 2, 3, 4, 2, "Goodbye")

first_occurrence = my_tuple.index(2)

print(f"The first occurrence of 2 is at index: {first_occurrence}.")
```

**Output:**

```text
The first occurrence of 2 is at index: 2.
```

**Using `count()`**

The `.count()` method returns the number of times a value occurs.

```python
count_of_twos = my_tuple.count(2)

print(f"The number 2 appears {count_of_twos} times in the tuple.")
```

**Output:**

```text
The number 2 appears 2 times in the tuple.
```

### Tuples Are Immutable

You cannot change an existing tuple element.

```python
my_tuple = (10, 20, 30)

# my_tuple[0] = 100  # TypeError
```

### Converting a Tuple into a List

If you need a mutable version of a tuple, you can convert it into a list using `list()`.

```python
my_tuple = ("Hello", 1, 2, 3)

my_list = list(my_tuple)
my_list[0] = "Python"

print(my_list)
```

**Output:**

```text
['Python', 1, 2, 3]
```

**Note:** A tuple containing a single element requires a trailing comma.

```python
single_element_tuple = (5,)

print(type(single_element_tuple))
```

**Output:**

```text
<class 'tuple'>
```

Without the comma, `(5)` is simply an integer expression inside parentheses.

---

## 7. Dictionaries

A **dictionary (`dict`)** is a collection that stores data as key-value pairs.

Each key is unique within a dictionary, while values can be repeated.

Dictionaries are created using curly braces `{}`.

### Creating Dictionaries

```python
# An empty dictionary
empty_dict = {}

# A dictionary containing key-value pairs
example_dict = {
    "name": "Alice",
    "age": 26,
    1: "integer_key",
    (1, 2): "tuple_key",
    "measurements": [0.5, 0.3]
}

print(example_dict)
```

A dictionary can contain different types of values. Its keys must be hashable, which commonly includes strings, numbers, and tuples whose elements are all hashable.

Lists and dictionaries cannot be used as dictionary keys because they are unhashable.

### Accessing Dictionary Values

Unlike lists and tuples, dictionary values are accessed using keys rather than numerical positions.

```python
example_dict = {
    "name": "Alice",
    "age": 26,
    "course": "Python"
}

print(example_dict["name"])
print(example_dict["age"])
```

**Output:**

```text
Alice
26
```

### Adding and Updating Values

You can use square brackets and the assignment operator to add a new key-value pair or update an existing value.

```python
example_dict = {
    "name": "Alice",
    "age": 26
}

# Update an existing value
example_dict["age"] = 27

# Add a new key-value pair
example_dict["course"] = "Python"

print(example_dict)
```

**Output:**

```text
{'name': 'Alice', 'age': 27, 'course': 'Python'}
```

### Using `get()`

The `.get()` method retrieves a value without raising a `KeyError` when the key is missing. By default, it returns `None` for a missing key.

```python
student = {
    "name": "Alice",
    "age": 26
}

print(student.get("name"))
print(student.get("grade"))
print(student.get("grade", "Not available"))
```

**Output:**

```text
Alice
None
Not available
```

### Checking Whether a Key Exists

Use the `in` operator to check whether a key exists in a dictionary.

```python
student = {
    "name": "Alice",
    "age": 26
}

print("name" in student)
print("grade" in student)
```

**Output:**

```text
True
False
```

### Removing a Key-Value Pair

The `.pop()` method removes a specified key and returns its value.

```python
student = {
    "name": "Alice",
    "age": 26,
    "course": "Python"
}

removed_value = student.pop("course")

print("Removed value:", removed_value)
print("Updated dictionary:", student)
```

**Output:**

```text
Removed value: Python
Updated dictionary: {'name': 'Alice', 'age': 26}
```

### Iterating Through a Dictionary

You can use `.items()` to access keys and values together.

```python
student = {
    "name": "Alice",
    "age": 26,
    "course": "Python"
}

for key, value in student.items():
    print(f"{key}: {value}")
```

**Output:**

```text
name: Alice
age: 26
course: Python
```

**Note:** Modern Python dictionaries preserve insertion order. However, their values are accessed by keys, not by list-style numerical indices.

---

## 8. Lists vs. Tuples vs. Dictionaries

| Feature | List | Tuple | Dictionary |
|---|---|---|---|
| Syntax | `[]` | `()` | `{key: value}` |
| Ordered | Yes | Yes | Yes, insertion order |
| Mutable | Yes | No | Yes |
| Allows duplicates | Yes | Yes | Keys must be unique |
| Access method | Index | Index | Key |
| Typical use | Modifiable collections | Fixed collections | Key-value mappings |

### When Should You Use Each?

- **List:** When you need an ordered collection that can be modified.
- **Tuple:** When you need an ordered collection that should not be structurally changed.
- **Dictionary:** When you need to associate values with meaningful, unique keys.

---

## 9. Summary

Python collections provide convenient ways to store and organize multiple values.

### Lists

- Created with square brackets `[]`.
- Ordered and mutable.
- Support indexing, slicing, and duplicate elements.
- Common methods include `.append()`, `.extend()`, `.remove()`, `.pop()`, and `.sort()`.

### Tuples

- Usually created with parentheses `()`.
- Ordered and immutable.
- Support indexing, slicing, `.count()`, and `.index()`.
- Can be converted into lists using `list()`.

### Dictionaries

- Created with curly braces `{}`.
- Store key-value pairs.
- Keys must be hashable and unique.
- Values can be of different types.
- Common methods include `.get()`, `.items()`, and `.pop()`.

---

## 10. Practice Exercises

Try solving the following exercises without looking at the examples above.

### Exercise 1: Create a List

Create a list containing five of your favorite fruits.

- Print the entire list.
- Print the first element.
- Print the last element.
- Print the first three elements using slicing.

### Exercise 2: Modify a List

Given the following list:

```python
numbers = [10, 20, 30, 40, 50]
```

- Change the first element to `100`.
- Append `60` to the list.
- Remove the element `30`.
- Sort the list in descending order.
- Print the final list.

### Exercise 3: Work with Tuples

Create a tuple containing the numbers `(1, 2, 3, 2, 4, 2)`.

- Find the first index of `2`.
- Count how many times `2` occurs.
- Convert the tuple into a list.

### Exercise 4: Create a Dictionary

Create a dictionary containing a student's name, age, and course.

- Print the student's name.
- Update the student's age.
- Add a new key called `"grade"`.
- Check whether `"course"` exists in the dictionary.

### Exercise 5: Predict the Output

Try to predict the output before running this code.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1])
print(numbers[-1])
print(numbers[1:4])
print(numbers[::-1])
```

### Exercise 6: Choose the Right Collection

Choose whether a list, tuple, or dictionary would be most appropriate for each situation:

1. Storing a shopping list that changes over time.
2. Storing the coordinates of a point as `(x, y)`.
3. Storing student names alongside their grades.


