# 🧰 Commonly Used Python Standard Libraries

Python comes with many built-in libraries that are incredibly useful for data science, scripting, automation, and real-world projects.

---

## 📂 1. `os` – Operating System Interface

```python
import os

print(os.getcwd())          # Get current directory
os.mkdir('new_folder')      # Create a new folder
os.listdir()                # List files in directory
```
- 📝 Use When: You need to interact with the file system or automate file/folder tasks.


---


## ⏱️ 2. datetime – Date and Time Handling

```python
from datetime import datetime, timedelta

now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M"))
```
- 📝 Use When: You’re working with timestamps, durations, or formatting dates.


---


## 🧮 3. math – Mathematical Functions

```python
import math

print(math.sqrt(16))       # Square root
print(math.ceil(2.3))      # Round up
print(math.pi)             # Value of π
```
- 📝 Use When: You need advanced mathematical functions (beyond + - * /).


---


## 🧪 4. random – Generate Random Numbers
```python
import random

print(random.randint(1, 10))        # Random integer
print(random.choice(['A', 'B']))    # Random element from list
```
- 📝 Use When: You want to generate random data, shuffle, or simulate randomness.


---


## 🧵 5. collections – Specialized Data Structures

```python
from collections import Counter

c = Counter(['a', 'b', 'a', 'c', 'b'])
print(c)  # Count of each element
```
- 📝 Use When: You need efficient counting, grouping, or dictionary operations.


---


## 🧰 6. itertools – Advanced Iterators

```python
from itertools import permutations

for p in permutations([1, 2, 3]):
    print(p)
```
- 📝 Use When: You’re working with combinations, permutations, or large loops.



---


## 🧪 7. json – Working with JSON Data

```python
import json

data = {'name': 'Alice', 'age': 25}
json_str = json.dumps(data)       # Convert to JSON string
parsed = json.loads(json_str)     # Parse JSON back to dict
```
- 📝 Use When: You need to send or receive data from APIs or store structured data.

---


## ✅ Summary
These built-in libraries are essential tools for writing powerful and efficient Python scripts. Mastering them makes your code cleaner and more production-ready.
---

## 🔗 Resources

📘 [Python Standard Library Docs](https://docs.python.org/3/library/index.html)  
📘 [W3Schools Python Modules](https://www.w3schools.com/python/python_modules.asp)
