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
~~~



class Calculation1:
    def Summation(self, a, b):
        return a + b


class Calculation2:
    def Subtraction(self, a, b):
        return a - b


class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero not allowed"


a = int(input("Enter first number: "))
b = int(input("Enter second number: "))


obj = Derived()
print("Summation:", obj.Summation(a, b))
print("Subtraction:", obj.Subtraction(a, b))
print("Division:", obj.Division(a, b))
~~~
## Output Example
Enter first number: 20
Enter second number: 5
## Result
The program successfully demonstrates multiple inheritance in Python. The Derived class inherits methods from both Calculation1 and Calculation2, while adding its own method for division. This allows a single object to perform addition, subtraction, and division operations.

