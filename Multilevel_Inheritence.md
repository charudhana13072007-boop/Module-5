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
~~~



class Person:
    def __init__(self, name):
        self.name = name
    
    def getName(self):
        return self.name


class Child(Person):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age
    
    def getAge(self):
        return self.age

class Grandchild(Child):
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location
    
    def getLocation(self):
        return self.location

name = input("Enter name: ")
age = int(input("Enter age: "))
location = input("Enter location: ")

obj = Grandchild(name, age, location)

print
~~~

## Sample Output
Enter name: Charumathi

Enter age: 22

Enter location: Tiruttani
## Result
The program successfully demonstrates multilevel inheritance in Python. The Grandchild class inherits attributes and methods from both Child and Person, allowing it to store and display a person’s name, age, and location.
