# 🔁 Loops and Conditional Statements in Python

Python provides powerful control flow tools to make decisions and repeat code. These are foundational for solving problems and building logic in real-world programs.

---

## 🔹 Conditional Statements

Used to execute certain blocks of code based on whether a condition is true.

### 🔹 Syntax

if condition:
    The if statement evaluates the condition and executes the block of code if the condition is True.
elif another_condition:
    The elif (short for "else if") is used to check additional conditions if the previous if or elif conditions were False.
else:
    The else block will execute if none of the preceding conditions are True.

```python
x = 10

if x > 0:
    print("Positive number")
elif x == 0:
    print("Zero")
else:
    print("Negative number")
```
Note: Python uses indentation (typically 4 spaces) to define code blocks. Curly braces {} are not used.

---


## 🧮 Comparison (Relational) Operators

These operators compare two values and return either True or False.

| Operator | Description              | Example  | Output  |
| -------- | ------------------------ | -------- | ------- |
| `==`     | Equal to                 | `5 == 5` | `True`  |
| `!=`     | Not equal to             | `3 != 4` | `True`  |
| `>`      | Greater than             | `10 > 7` | `True`  |
| `<`      | Less than                | `2 < 8`  | `True`  |
| `>=`     | Greater than or equal to | `5 >= 5` | `True`  |
| `<=`     | Less than or equal to    | `6 <= 3` | `False` |


## 🔗 Logical Operators

Used to combine multiple conditions together.

| Operator | Description                      | Example               | Result  |
| -------- | -------------------------------- | --------------------- | ------- |
| `and`    | True if both conditions are true | `(5 > 2) and (3 < 4)` | `True`  |
| `or`     | True if at least one is true     | `(5 < 2) or (3 < 4)`  | `True`  |
| `not`    | Inverts the boolean value        | `not (5 > 2)`         | `False` |


🔹 Example
```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive!")
```


---


## 🔄 Loops in Python

Loops allow you to execute a block of code multiple times.


###🔸 For Loop

Used to iterate over a sequence like a list, tuple, or a range.

```python
for i in range(5):
    print(i)  # Outputs: 0 1 2 3 4
```

🔹 Looping over strings or lists

```python
for char in "hello":
    print(char)

names = ["Alice", "Bob", "Charlie"]
for name in names:
    print(name)
```
### 🔸 While Loop

Repeats a block of code as long as a condition is true.

```python
count = 0
while count < 5:
    print(count)
    count += 1
```
Be careful with while loops — if the condition never becomes false, the loop will run forever (infinite loop).


## ⏹️ Loop Control Statements

These are used to control the behavior of loops.

| Statement  | Description                          | Example Use                                                                       |
| ---------- | ------------------------------------ | --------------------------------------------------------------------------------- |
| `break`    | Exits the loop prematurely           | Stop loop if a condition is met                                                   |
| `continue` | Skips the current iteration          | Skip specific values during loop                                                  |
| `pass`     | Does nothing (used as a placeholder) | Used when a statement is syntactically required but you don’t want to do anything |


🔹 break Example
```python
for i in range(5):
    if i == 3:
        break
    print(i)  # Outputs: 0, 1, 2
```

🔹 continue Example
```python
for i in range(5):
    if i == 3:
        continue
    print(i)  # Outputs: 0, 1, 2, 4
```

🔹 pass Example
```python
for i in range(5):
    if i == 3:
        pass  # Does nothing
    print(i)
```

---

## 🧠 Key Takeaways

- Use if, elif, and else for decision-making.
- Use comparison operators to evaluate conditions.
- Combine conditions using logical operators.
- Use for loops to iterate over a sequence.
- Use while loops for conditional repetition.
- Control loop execution using break, continue, and pass.


## 🔗 Resources

- [📘 Python if...else (W3Schools)](https://www.w3schools.com/python/python_conditions.asp)
- [📘 Python Loops (W3Schools)](https://www.w3schools.com/python/python_for_loops.asp)
- [📘 Python Loop Control Statements (GeeksforGeeks)](https://www.geeksforgeeks.org/loops-in-python/)




