# 📂 File Handling in Python

File handling allows you to create, read, update, and delete files using Python. This is essential for working with data stored outside your program.

---

## 📁 Opening a File

Use the `open()` function with the filename and mode:

```python
file = open("example.txt", "r")  # Open for reading
```

---


### 📌 Common File Modes

| Mode | Description |
|------|-------------|
| `"r"` | Read (default mode). Opens the file for reading. Error if the file does not exist. |
| `"w"` | Write. Creates a new file or truncates the file if it exists. |
| `"a"` | Append. Opens the file for writing; data is added at the end of the file. |
| `"x"` | Create. Creates a new file. Returns an error if the file already exists. |
| `"b"` | Binary mode. Used to read/write binary files (e.g., `"rb"`, `"wb"`). |
| `"t"` | Text mode. Default mode. Used to read/write text files. |


---

## 📖 Reading from a File

```python
file = open("example.txt", "r")
content = file.read()
print(content)
file.close()
```

Or read line by line

```python
file = open("example.txt", "r")
for line in file:
    print(line.strip())
file.close()
```

## ✍ Writing to a File

```python
file = open("example.txt", "w")
file.write("Hello, World!\n")
file.write("Welcome to file handling in Python.")
file.close()
```

## 📝 Appending to a File

```python
file = open("example.txt", "a")
file.write("\nThis line will be added at the end.")
file.close()
```

### ✅ Using with Statement (Best Practice)

Automatically closes the file when done:

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```















