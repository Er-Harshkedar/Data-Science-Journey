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
