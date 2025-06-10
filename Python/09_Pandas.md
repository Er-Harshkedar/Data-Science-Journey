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
