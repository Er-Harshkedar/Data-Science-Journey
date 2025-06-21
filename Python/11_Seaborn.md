# 📊 Seaborn – Statistical Data Visualization

**Seaborn** is a Python library based on Matplotlib that provides a high-level interface for drawing attractive and informative statistical graphics — especially from DataFrames.

```python
import seaborn as sns
import matplotlib.pyplot as plt
```

## 📌 Why Use Seaborn?

- Beautiful, default themes
- Built-in support for Pandas DataFrames
- Easy plotting of statistical patterns (like histograms, box plots, correlations)

## 📈 1. Line Plot
```python
sns.lineplot(x=[1, 2, 3], y=[5, 8, 6])
plt.title("Line Plot")
plt.show()
```
**📝 Use When: You want to see trends over a continuous variable.**

---

## 📊 2. Bar Plot
```python
import pandas as pd

df = pd.DataFrame({'Category': ['A', 'B', 'C'], 'Values': [5, 8, 3]})
sns.barplot(x='Category', y='Values', data=df)
plt.title("Bar Plot")
plt.show()
```

**📝 Use When: You want to compare mean values across categories.**


---


