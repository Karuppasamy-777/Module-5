# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
# 1. Define Calculation1 class
class Calculation1:
    # Method to return the sum of two numbers
    def Summation(self, a, b):
        return a + b

# 2. Define Calculation2 class
class Calculation2:
    # Method to return the difference of two numbers
    def Subtraction(self, a, b):
        return a - b

# 3. Define Derived class inheriting from both parent classes
class Derived(Calculation1, Calculation2):
    # Method to return the division result
    def Division(self, a, b):
        if b == 0:
            return "Error! Division by zero is not allowed."
        return a / b

# 4. Input & Execution Block
if __name__ == "__main__":
    # Prompt the user to enter two numbers
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    # 5. Create an object of the Derived class
    calc = Derived()

    # Process and call Summation, Subtraction, and Division methods
    add_result = calc.Summation(num1, num2)
    sub_result = calc.Subtraction(num1, num2)
    div_result = calc.Division(num1, num2)

    # 6. Output the results
    print("\n--- Arithmetic Results ---")
    print(f"Addition: {num1} + {num2} = {add_result}")
    print(f"Subtraction: {num1} - {num2} = {sub_result}")
    print(f"Division: {num1} / {num2} = {div_result}")
```
## Output Example
```
Enter first number: 12
Enter second number: 4

--- Arithmetic Results ---
Addition: 12.0 + 4.0 = 16.0
Subtraction: 12.0 - 4.0 = 8.0
Division: 12.0 / 4.0 = 3.0
```
