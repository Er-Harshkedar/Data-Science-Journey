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


## 🎯 3. Count Plot
```python
sns.countplot(x='Category', data=df)
```
**📝 Use When: You want to count how many times each category occurs.**



---


## 🔵 4. Scatter Plot
```python
tips = sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', data=tips)
plt.title("Tip vs. Total Bill")
plt.show()
```
**📝 Use When: You want to observe relationships between two numeric variables.**



---


## 📦 5. Box Plot
```python
sns.boxplot(x='day', y='total_bill', data=tips)
```
**📝 Use When: You want to visualize distributions and outliers.**


---


## 🌡️ 6. Heatmap (Correlation Matrix)
```pytho
corr = tips.corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.title("Correlation Heatmap")
plt.show()
```
**📝 Use When: You want to show correlation between numeric variables.**


---


## 🎨 Customizing Seaborn Plots
- Use hue= to break data by category
- Use palette= to change color scheme
- Use style= and context= for theme control

```python
sns.set(style="whitegrid", context="talk")
```


## ✅ Summary
Seaborn makes it simple to create beautiful and insightful visualizations with very little code. It's especially powerful when working with structured data in Pandas DataFrames.
