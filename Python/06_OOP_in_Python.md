# 🧱 Object-Oriented Programming (OOP) in Python

Object-Oriented Programming is a programming paradigm built around the concept of **classes** and **objects**. It helps in organizing code for better readability, reusability, and scalability.

---

## 1. 🐾 What Are Classes and Objects?

In Python, everything is an object. A **class** is like a blueprint for creating **objects**.

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} says Woof!")

my_dog = Dog("Bruno")
my_dog.speak()  # Output: Bruno says Woof!
```
- $Dog$ is a class.
- $my_dog$ is an object (or instance) of the class.
- $__init__$ is a special method called a constructor that runs when an object is created.


---


## 2. 🔁 Inheritance (Reusing Code)

Inheritance allows one class to acquire the properties and methods of another.
The new class is the child (subclass) and the original is the parent (superclass).

```python
class Animal:
    def move(self):
        print("Animal moves")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

pet = Dog()
pet.move()  # Inherited from Animal
pet.bark()  # Defined in Dog
```
🧠 Inheritance promotes code reuse and simplifies large programs.


---


## 3. 🌈 Polymorphism (One Name, Many Forms)

Polymorphism allows different classes to define methods with the same name, and Python decides which one to call at runtime.

```python
class Cat:
    def speak(self):
        print("Meow")

class Dog:
    def speak(self):
        print("Woof")

for animal in [Cat(), Dog()]:
    animal.speak()
```
- Both Cat and Dog have a speak() method.
- The same method name works differently depending on the object.


---


## 4. 🔐 Encapsulation (Hiding the Data)

Encapsulation means keeping data safe by restricting direct access. Private variables are indicated with double underscores $__$.

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # private variable

    def deposit(self, amount):
        self.__balance += amount
        print("Deposit successful")
```

- Encapsulation ensures data protection and allows access only through defined methods.



---


## 5. 🧊 Abstraction (Hiding Complexity)

Abstraction means showing only the essential features while hiding the internal details.

- Abstract classes are created using abc module (advanced usage)
- Concept: expose only what is needed and hide unnecessary details



---


## 📌 Summary

- Class: A blueprint for creating objects.
- Object: An instance of a class.
- Inheritance: Reuse code by extending existing classes.
- Polymorphism: Same method name behaves differently in different classes.
- Encapsulation: Restrict access to protect data.
- Abstraction: Hide complex logic and show only what's necessary.

These OOP principles are fundamental in building real-world software and systems. 🧠🐍


---

## 🔗 Resources

- 📘 [Python OOP (W3Schools)](https://www.w3schools.com/python/python_classes.asp)  
- 📘 [Object-Oriented Programming in Python (GeeksforGeeks)](https://www.geeksforgeeks.org/python-object-oriented-programming/)
