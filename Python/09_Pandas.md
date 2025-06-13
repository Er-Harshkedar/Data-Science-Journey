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

### 🔍 Accessing Elements

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


# Output:
     Name  Age      City
0   Alice   25  New York
1     Bob   30     Paris
2  Charlie   35    London
```


---


### 🔍 Accessing Data in a DataFrame

Pandas offers flexible ways to access data from a DataFrame, whether by column, row, or individual cell.

---

#### 📌 Accessing Columns
```python
df['Name']           # Access a single column
df[['Name', 'Age']]  # Access multiple columns
```

#### 📌 Accessing Rows

```python
df.iloc[0]      # Access by row index (integer location)
df.loc[0]       # Access by row label (same as iloc if default index)
```
- iloc[] is used for positional indexing (0-based).
- loc[] is used for label-based indexing (especially after custom indexing).


#### 📌 Accessing a Cell
```python
df.loc[1, 'City']     # Get value from row 1, column 'City'
df.iloc[1, 2]         # Same using position (row 1, column 2)
```
- Combines row and column access.
- Returns a single value (scalar).


---



### 🧠 Descriptive Statistics in Pandas

Pandas provides powerful built-in functions to quickly understand your dataset.

---

#### 📊 `df.describe()`
Returns a summary of statistics for numeric columns, including:
- **count** – Number of non-null values
- **mean** – Average value
- **std** – Standard deviation
- **min**, **25%**, **50% (median)**, **75%**, **max** – Distribution percentiles

```python
df.describe()
```

ℹ️ df.info()

- Gives a concise summary of the DataFrame:
- Number of entries
- Column names and data types
- Non-null counts
- Memory usage

```python 
df.info()
```


👀 df.head(n) / df.tail(n)
- df.head() returns the first n rows (default = 5)
- df.tail() returns the last n rows (default = 5)

```python
df.head()
df.tail(3)
```

---


## 📥 Loading Data in Pandas

Pandas makes it easy to load data from different file formats like CSV, Excel, and more.

---

### 📄 Loading CSV Files

```python
import pandas as pd

df = pd.read_csv('data.csv')
print(df.head())
```
- read_csv() is the most common way to import tabular data.
- df.head() shows the first 5 rows to give a quick overview.
- CSV files are widely used in data science for storing structured data.


---


## 🔍 Filtering Data in Pandas

Filtering allows you to select rows that meet certain conditions — similar to WHERE clauses in SQL.

This is useful when you only want to work with specific subsets of your data, like finding users above a certain age, or products with high sales.

---

### 🧪 Example: Filtering with Conditions

```python
import pandas as pd

data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 32, 30, 28],
    'City': ['NY', 'Paris', 'London', 'NY']
}

df = pd.DataFrame(data)

# Filter: People older than 28
df[df['Age'] > 28]
```


### 🔗 Combining Multiple Conditions
```python
# AND condition
df[(df['Age'] > 28) & (df['City'] == 'NY')]

# OR condition
df[(df['Age'] > 28) | (df['City'] == 'Paris')]
```
- Use & for AND, | for OR
- Wrap each condition in parentheses!


### ❓ Filtering by Text Match
```python
df[df['City'] == 'NY']
```

