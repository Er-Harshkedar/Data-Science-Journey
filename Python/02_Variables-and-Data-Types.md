# 🧮 Variables and Data Types in Python

Variables are containers used to store data values. In Python, you don't need to declare the type of variable explicitly — it's dynamically inferred.

---

## 🔹 Declaring Variables

```python
name = "Harsh"        # string
age = 23              # integer
height = 5.9          # float
is_student = True     # boolean
```

## 🔹Common Data Types in Python

| Data Type | Example         | Description                   |
| --------- | --------------- | ----------------------------- |
| `int`     | `10`, `-3`      | Whole numbers                 |
| `float`   | `3.14`, `-2.0`  | Decimal numbers               |
| `str`     | `"hello"`       | Textual data                  |
| `bool`    | `True`, `False` | Boolean values                |
| `list`    | `[1, 2, 3]`     | Ordered, mutable collection   |
| `tuple`   | `(1, 2, 3)`     | Ordered, immutable collection |
| `dict`    | `{"a": 1}`      | Key-value pairs (dictionary)  |
| `set`     | `{1, 2, 3}`     | Unordered, unique values      |


---

## 🔀 Mutable vs Immutable Types

### ✅ Mutable Types
- Can be changed after creation.
- Examples: `list`, `dict`, `set`

```python
my_list = [1, 2, 3]
my_list[0] = 99
print(my_list)  # [99, 2, 3]
```

### 🚫 Immutable Types
- Cannot be changed after creation.
- Examples: int, float, str, tuple, bool

```python
x = 5
x = x + 1   # This creates a new int object; `x` now points to 6

text = "hello"
text[0] = "H"  # ❌ Error: strings are immutable
```

### 🧠 Why It Matters
- Mutable types can be modified in place, which is useful for performance but can lead to bugs if not handled carefully.
- Immutable types are safe from unintended changes, especially when passed between functions or used as dictionary keys.


---


## 🔄 Type Checking and Conversion

```python
print(type(name))      # <class 'str'>
print(type(age))       # <class 'int'>

# Type conversion
age_str = str(age)
height_int = int(height)
```

## 🧠 Key Takeaways

- Variables in Python are dynamically typed.
- You can reassign variables to different data types.
- Use type() to check a variable's data type.
- Use built-in functions like str(), int(), float() to convert types.

---


## 🔗 Resources

- [📘 Python Variables (W3Schools)](https://www.w3schools.com/python/python_variables.asp)
- [📘 Python Data Types (GeeksforGeeks)](https://www.geeksforgeeks.org/python-data-types/)

