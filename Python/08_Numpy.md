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

##⚡ Why Are NumPy Arrays Faster Than Python Lists?

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




