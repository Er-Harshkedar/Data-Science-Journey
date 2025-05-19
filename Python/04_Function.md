# 🐍 Functions in Python

Functions are reusable blocks of code designed to perform a specific task. They help break programs into smaller, modular pieces and avoid repetition.

---

## 📋 Defining a Function

Use the `def` keyword followed by the function name and parentheses:

```python
def greet():
    print("Hello, world!")

# Call the function by its name with parentheses:
greet()  # Output: Hello, world!

```

---

## 🔹 Function Parameters and Arguments

Functions can take inputs called parameters to work with different values:

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
```

---

## 🔹 Returning Values

Functions can return values using the return statement:

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

---

## 🔹 Default Parameters

You can provide default values to parameters:

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()         # Output: Hello, Guest!
greet("Bob")    # Output: Hello, Bob!
```

---

## 🔹 Variable-length Arguments: *args and **kwargs

- *args allows passing a variable number of positional arguments.
  ```python
  def add_all(*args):
    return sum(args)
  
  print(add_all(1, 2, 3, 4))  # Output: 10
  ```

- **kwargs allows passing a variable number of keyword arguments.

```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25)
#output name: Alice
#age: 25
```

---

## 🔹 Lambda Functions (Anonymous Functions)

Small, unnamed functions useful for simple operations:

```python
square = lambda x: x * x
print(square(5))  # Output: 25
```

---


## 🔗 Resources

- [Python Functions (W3Schools)](https://www.w3schools.com/python/python_functions.asp)  
- [Functions in Python (GeeksforGeeks)](https://www.geeksforgeeks.org/python-functions/)


  

