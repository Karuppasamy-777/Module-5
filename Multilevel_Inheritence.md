# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```
# 1. Parent Class
class Parent:
    def __init__(self, name):
        # Initializes the name attribute
        self.name = name

    def getName(self):
        return self.name


# 2. Child Class (inherits Parent)
class Child(Parent):
    def __init__(self, name, age):
        # Initializes name using super() and adds age
        super().__init__(name)
        self.age = age

    def getAge(self):
        return self.age


# 3. Grandchild Class (inherits Child)
class Grandchild(Child):
    def __init__(self, name, age, location):
        # Initializes name and age using super() and adds location
        super().__init__(name, age)
        self.location = location

    def getLocation(self):
        return self.location


# 4. Input & Output Execution
if __name__ == "__main__":
    # Take user input for name, age, and location
    user_name = input("Enter Name: ")
    user_age = input("Enter Age: ")
    user_location = input("Enter Location: ")

    # Create an instance of Grandchild
    person = Grandchild(user_name, user_age, user_location)

    # Print all details using class methods
    print("\n--- Person Details ---")
    print(f"Name: {person.getName()}")
    print(f"Age: {person.getAge()}")
    print(f"Location: {person.getLocation()}")
```
## Sample Output
```
Enter Name: Jessica
Enter Age: 28
Enter Location: New York

--- Person Details ---
Name: Jessica
Age: 28
Location: New York
```
