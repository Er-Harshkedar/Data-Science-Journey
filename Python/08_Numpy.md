# 🧮 NumPy (Numerical Python)

## 📌 Introduction
NumPy (Numerical Python) is a fundamental library for numerical computing in Python. It provides efficient array operations, mathematical functions, and tools for working with large datasets. It's the backbone for most Python data science libraries like Pandas, Scikit-learn, TensorFlow, etc.

---

## ⚙️ Installation

To install NumPy, run:

```bash
pip install numpy
```

Numpy provides the ndarray (n-dimensional array) which is faster and more memory-efficient than Python lists.

## ⚡ Why Are NumPy Arrays Faster Than Python Lists?

NumPy arrays are significantly faster than Python lists because of how they store data in memory:

- **Contiguous Memory Allocation:** NumPy arrays store all elements in a **contiguous block of memory** of the same data type. This makes it efficient for CPU-level operations and allows for **vectorized operations** (processing many elements at once).
  
- **Python Lists Store References:** In contrast, Python lists are **collections of references** to objects stored at different memory locations. This means extra time is needed to resolve each reference during operations.


### 🔍 Performance Comparison Example

```python
import numpy as np
import time

# Using NumPy
arr = np.arange(1000000)
start = time.time()
arr_squared = arr ** 2
end = time.time()
print("NumPy Time:", end - start)

# Using List
lst = list(range(1000000))
start = time.time()
lst_squared = [x ** 2 for x in lst]
end = time.time()
print("List Time:", end - start)

```
🕐 You'll typically see that NumPy is 4-10x faster than lists in such operations.



---


## 📊 Creating NumPy Arrays

```python
import numpy as np

# Creating arrays
arr1 = np.array([1, 2, 3])
arr2 = np.array([[1, 2], [3, 4]])
```

OR

Simplest possible: We use a list as an argument input in making a NumPy Array

```python
# Create array from Python list
list1 = [1, 2, 3, 4]
data = np.array(list1)
data

# Output:  array([1, 2, 3, 4])
```

```python
# See data type that is stored in the array
data.dtype

# The data types are specified for the full array, if we store
# a float in an int array, the float will be up-casted to an int
data[0] = 3.14159
data
# Output: array([3, 2, 3, 4])

# NumPy converts to most logical data type
data2 = np.array([1.2, 2, 3, 4])
print(data2)
print(data2.dtype) # all values will be converted to floats

# Output: [1.2 2.  3.  4. ]
float64
# We can manually specify the datatype
data3 = np.array([1, 2, 3], dtype=str)
print(data3)
```


---


## 🔍 Indexing and Slicing

```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[1])       # Output: 20
print(arr[1:4])     # Output: [20 30 40]

# more slicing
x = np.array(range(18))
print ('x:',x)     # Output: x: [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17]
print (x[5:15:2])  # Output: [ 5  7  9 11 13]
```


---


## ➕ Basic Array Operations
```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print(a + b)        # [5 7 9]
print(a * b)        # [4 10 18]
print(a ** 2)       # [1 4 9]

# if you need to join numpy arrays,
# try hstack, vstack, column_stack, or concatenate
np.hstack([a, bb])       # [1,2,3,4,5,6]
np.column_stack([a, b])  # [[1,4],
                            [2,5],
                            [3,6]]
```


---


## 🔁 Useful NumPy Functions

