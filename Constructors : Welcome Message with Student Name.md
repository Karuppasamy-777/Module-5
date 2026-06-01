# # Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program
```
class Student:
    def __init__(self):
        # 1 & 3. Get user input and assign it to the instance variable self.a
        self.a = input("Enter the student's name: ")

    # 4. Define a method to display the required messages
    def show(self):
        print("This is non-parameterized constructor")
        print(f"Welcome, {self.a}!")
```
# 5. Execute the Program: Instantiate the class and call the show method
student_object = Student()
student_object.show()
## Output
```
Enter the student's name: Alex
This is non-parameterized constructor
Welcome, Alex!
```
## Result
the resultof the python program is verified
