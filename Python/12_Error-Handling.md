# ⚠️ Python Error Handling

Errors are common during code execution — whether it's a file not found, division by zero, or invalid input. Python lets you handle these gracefully using **try/except** blocks.

---

## 🔥 Types of Errors

1. **Syntax Errors** – Mistakes in code structure.
2. **Runtime Errors** – Occur while the code is running (e.g., ZeroDivisionError).
3. **Logical Errors** – Code runs, but the result is incorrect.

---

## 🧪 Basic Try-Except Block

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")
```
📌 Use When: You expect certain operations might fail and want to avoid crashes.




## 🛠️ Catching Multiple Exceptions
```python
try:
    file = open("data.txt", "r")
    value = int("abc")
except FileNotFoundError:
    print("File not found.")
except ValueError:
    print("Invalid type conversion.")
```


---


## ✅ Else and Finally Blocks
```python
try:
    result = 5 / 1
except ZeroDivisionError:
    print("Error!")
else:
    print("No error occurred.")
finally:
    print("Always runs, error or not.")
```
- else: Runs only if no exception occurs.
- finally: Always runs — useful for cleanup


---


## 📦 Raising Custom Exceptions
```python
def check_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    return age

check_age(-5)
```
**📌 Use When: You want to define and raise your own error messages.**


## 🧰 Best Practices
- Use specific exceptions (not just except:).
- Use finally to close files or release resources.
- Don't silence errors without logging them.


---


## ✅ Summary
Error handling allows you to write safer, more reliable code that doesn't break unexpectedly. It’s essential for writing production-quality applications.


---


## 🔗 Resources

📘 [Python Try-Except – W3Schools](https://www.w3schools.com/python/python_try_except.asp)  
📘 [Python Errors and Exceptions – Official Docs](https://docs.python.org/3/tutorial/errors.html)
