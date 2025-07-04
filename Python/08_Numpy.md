# 🧮 NumPy (Numerical Python)

## 📌 Introduction
NumPy (Numerical Python) is a fundamental library for numerical computing in Python. It provides efficient array operations, mathematical functions, and tools for working with large datasets. It's the backbone for most Python data science libraries like Pandas, Scikit-learn, TensorFlow, etc.

---

## ⚙️ Installation

To install NumPy, run:

```bash
pip install numpy
```

---


**Numpy provides the ndarray (n-dimensional array) which is faster and more memory-efficient than Python lists.**

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
print (x[5:15:2])  # Output: [ 5  7  9 11 13] , It prints every 2nd element from index 5 to 14 in the array x.
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


## Attributes of a multidim array
```python
data = np.array([[1, 2, 3], [4, 5, 6]])
data = np.array(list3)


print('Dimensions:',data.ndim)   # Dimensions: 2
print ('Shape:',data.shape)      # Shape: (2, 3)
print('Size:', data.size)        # Size: 6
```


```python
# You can also transpose an array Matrix with either np.transpose(arr)
# or arr.T
data.T

''' Output: array([[1, 4],
                   [2, 5],
                   [3, 6]])'''

```

---


##  Vectorization and Broadcasting

- Broadcasting allows NumPy to perform arithmetic operations on arrays of different shapes without explicit looping. This can simplify code and improve performance by leveraging low-level optimizations.

```python
import numpy as np

# Create a 2D array (3x4)
arr_2d = np.array([[1, 2, 3, 4],
                   [5, 6, 7, 8],
                   [9, 10, 11, 12]])

# Create a 1D array (4,)
arr_1d = np.array([[10], [20], [30]])

# Add the 1D array to each row of the 2D array
result = arr_2d + arr_1d

print("2D array:\n", arr_2d)
print("1D array:\n", arr_1d)
print("Result of broadcasting:\n", result)

''' Output : 2D array:
 [[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]]
1D array:
 [[10]
 [20]
 [30]]
Result of broadcasting:
 [[11 12 13 14]
 [25 26 27 28]
 [39 40 41 42]]'''
```


- Vectorization refers to the ability to perform operations on entire arrays or portions of arrays at once, rather than using explicit loops. This is often more efficient and concise.


```python
import numpy as np

# Create an array
arr = np.array([1, 2, 3, 4, 5])

# Compute the square of each element using vectorization
squared = arr ** 2

print("Original array:\n", arr)
print("Squared array:\n", squared)

''' Output: Original array:
 [1 2 3 4 5]
Squared array:
 [ 1  4  9 16 25]'''
```

---

## 🔁 Useful NumPy Functions
```python
np.zeros((2, 3))      # 2x3 array of zeros

np.ones((2, 2))       # 2x2 array of ones

np.eye(3)             # Identity matrix

np.arange(0, 10, 2)   # [0 2 4 6 8]
'''np.arange() is similar to built in range()
Creates array with a range of consecutive numbers
starts at 0 and step=1 if not specified. Exclusive of stop.'''


np.linspace(0, 1, 5)  # [0.   0.25 0.5  0.75 1. ]
# linspace: Create an array of numbers from a to b
# with n equally spaced numbers (inclusive)


```


---

## 🔃 Reshaping

```python
# Reshape is used to change the shape
a = np.arange(0, 15)

print('Original:',a)
a = a.reshape(3, 5)
# a = np.arange(0, 15).reshape(3, 5)  # same thing
print ('Reshaped:')
print(a)

'''Output: Original: [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14]
Reshaped:
[[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]'''


# We can also easily find the sum, min, max, .. are easy
print (a)
print ('Sum:',a.sum())
print('Min:', a.min())
print('Max:', a.max())

'''[[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]]

Sum: 105
Min: 0
Max: 14'''
``` 


---


## 💡 Why NumPy for Data Science?

- Faster than Python lists (due to fixed type and vectorization)
- Makes matrix and linear algebra operations easy
- Supports broadcasting and advanced indexing
- Foundation for libraries like Pandas and Scikit-learn



--- 


### 🔗 Resources

📘 [NumPy Tutorial (W3Schools)](https://www.w3schools.com/python/numpy_intro.asp)  
📘 [NumPy Basics (GeeksforGeeks)](https://www.geeksforgeeks.org/numpy-tutorial/)  
📘 [NumPy User Guide (Official Docs)](https://numpy.org/doc/stable/user/)  


--- 


## 🚀 Use Cases of NumPy

NumPy is a powerful tool used across many fields in data and scientific computing. Here are some of its key use cases:

- **Data Analysis:** Fast computations on large datasets.
- **Machine Learning:** Core operations like vectorization and data transformation.
- **Scientific Computing:** Simulations, numerical modeling, and engineering calculations.
- **Image & Signal Processing:** Manipulating pixels and signals as numerical arrays.
- **Linear Algebra:** Matrix operations, solving equations, and transformations.
- **Financial Modeling:** Time series data, simulations, and statistics.

We'll explore many of these areas in detail later in this repository.

