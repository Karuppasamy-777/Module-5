# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
# 1. Base class with common attributes
class Details:
    def getName(self):
        self.name = input("Enter Name: ")
        
    def getAge(self):
        self.age = input("Enter Age: ")


# 2. Derived Class 1: Inherits from Details
class Employee(Details):
    def getEmployeeDetails(self):
        print("\n--- Enter Employee Details ---")
        self.getName()  # Inherited method
        self.getAge()   # Inherited method
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")

    def displayEmployee(self):
        print("\n--- Employee Information ---")
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")
        print(f"Employee ID: {self.employee_id}")
        print(f"Department: {self.department}")


# 3. Derived Class 2: Inherits from Details
class Patient(Details):
    def getPatientDetails(self):
        print("\n--- Enter Patient Details ---")
        self.getName()  # Inherited method
        self.getAge()   # Inherited method
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")

    def displayPatient(self):
        print("\n--- Patient Information ---")
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")
        print(f"Patient ID: {self.patient_id}")
        print(f"Disease: {self.disease}")


# 4 & 5. Get user input and display collected information
if __name__ == "__main__":
    # Manage Employee
    emp = Employee()
    emp.getEmployeeDetails()
    
    # Manage Patient
    pat = Patient()
    pat.getPatientDetails()
    
    # Display Results
    emp.displayEmployee()
    pat.displayPatient()
```
## Sample Output
```
--- Enter Employee Details ---
Enter Name: Alice Smith
Enter Age: 34
Enter Employee ID: EMP101
Enter Department: Engineering

--- Enter Patient Details ---
Enter Name: Bob Jones
Enter Age: 45
Enter Patient ID: PAT902
Enter Disease: Flu

--- Employee Information ---
Name: Alice Smith
Age: 34
Employee ID: EMP101
Department: Engineering

--- Patient Information ---
Name: Bob Jones
Age: 45
Patient ID: PAT902
Disease: Flu
```
## Result
the uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details is verified
