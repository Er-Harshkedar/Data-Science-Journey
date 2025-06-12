# 📊 Introduction to Pandas

Pandas is a powerful open-source Python library used for data analysis and manipulation. It is built on top of NumPy and provides easy-to-use data structures like:

- **Series**: One-dimensional labeled arrays.
- **DataFrame**: Two-dimensional labeled data structures (like a spreadsheet or SQL table).

Pandas allows you to:
- Load and explore datasets from various sources (CSV, Excel, SQL, etc.)
- Clean, filter, and transform data efficiently
- Perform complex data analysis and aggregations with minimal code


## 🧱 Pandas Series

A **Series** is a one-dimensional labeled array that can hold any data type — integers, strings, floats, Python objects, etc.

It’s like a column in a spreadsheet or database.

### ✅ Creating a Series

```python
import pandas as pd

# From a list
data = [10, 20, 30, 40]
s = pd.Series(data)
print(s)

# Output :0    10
1    20
2    30
3    40
dtype: int64
```
You can also set custom labels (index):

```python
s = pd.Series([10, 20, 30], index=['a', 'b', 'c'])
print(s)

# Output:
a    10
b    20
c    30
dtype: int64
```

🔍 Accessing Elements

```python
print(s['a'])     # Access by label → 10
print(s[0])       # Access by position → 10
```

🛠️ Useful Attributes and Methods
```python
s.values      # returns array([10, 20, 30])
s.index       # returns Index(['a', 'b', 'c'], dtype='object')
s.sum()       # returns 60
s.mean()      # returns 20.0
```



---


## 🧩 Pandas DataFrame

A **DataFrame** is a two-dimensional, size-mutable, and heterogeneous data structure with labeled axes (rows and columns). Think of it like a table in SQL or an Excel spreadsheet.

### ✅ Creating a DataFrame

```python
import pandas as pd

# From a dictionary
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Paris', 'London']
}

df = pd.DataFrame(data)
print(df)


# Output:      Name  Age      City
0   Alice   25  New York
1     Bob   30     Paris
2  Charlie   35    London
```
