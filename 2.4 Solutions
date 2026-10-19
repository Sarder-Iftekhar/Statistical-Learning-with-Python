
# 1. Variables
name = "Rahim"
age = 22
height = 5.8

print(name)
print(age)
print(height)


# 2. Types
number = 10
price = 19.99
message = "Hello Python"
is_learning = True

print(type(number))
print(type(price))
print(type(message))
print(type(is_learning))


# 3. Strings
first_name = "Rahim"
last_name = "Ahmed"

full_name = first_name + " " + last_name
print(full_name)

print(full_name.upper())
print(full_name.lower())
print(len(full_name))


# 4. Booleans
age = 20

is_adult = age >= 18
print(is_adult)

print(10 > 5)
print(10 == 5)
print(10 != 5)


# 5. Lists
fruits = ["apple", "banana", "mango"]

print(fruits)
print(len(fruits))

fruits.append("orange")
print(fruits)

fruits.remove("banana")
print(fruits)


# 6. More Lists
numbers = [10, 20, 30, 40, 50]

print(numbers[0])
print(numbers[-1])

numbers[1] = 25
print(numbers)

numbers.append(60)
print(numbers)

numbers.pop()
print(numbers)


# 7. Indexing and Slicing
letters = ["a", "b", "c", "d", "e"]

print(letters[0])
print(letters[-1])
print(letters[1:4])
print(letters[:3])
print(letters[2:])


# 8. Dictionaries
student = {
    "name": "Rahim",
    "age": 22,
    "grade": 85
}

print(student["name"])
print(student["age"])

student["grade"] = 90
student["city"] = "Dhaka"

print(student)


# 9. Voluntary Exercise: Lists and Dictionaries
students = [
    {"name": "Rahim", "grade": 80},
    {"name": "Karim", "grade": 90},
    {"name": "Ayesha", "grade": 95},
]

for student in students:
    print(student["name"], student["grade"])


# 10. Voluntary Exercise: Highest Average Grade
students = [
    {"name": "Rahim", "grades": [80, 85, 90]},
    {"name": "Karim", "grades": [75, 88, 82]},
    {"name": "Ayesha", "grades": [95, 92, 98]},
]

highest_average = -1
top_student = ""

for student in students:
    average = sum(student["grades"]) / len(student["grades"])
    print(student["name"], "Average:", average)

    if average > highest_average:
        highest_average = average
        top_student = student["name"]

print("Highest average:", top_student)
print("Average grade:", highest_average)


# 11. Voluntary Exercise: Swap Without a Temporary Variable
a = 10
b = 20

a, b = b, a

print("a =", a)
print("b =", b)
