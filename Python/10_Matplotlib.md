# 📈 Introduction to Matplotlib

**Matplotlib** is a powerful Python library used for creating static, animated, and interactive visualizations. It’s widely used in data science for plotting data trends, patterns, and distributions.

---

## 🛠️ Basic Setup

```python
import matplotlib.pyplot as plt
# You typically use the alias plt when importing Matplotlib’s pyplot module.

# 📌 Plotting a Simple Line Graph

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.title("Simple Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.grid(True)
plt.show()
```


