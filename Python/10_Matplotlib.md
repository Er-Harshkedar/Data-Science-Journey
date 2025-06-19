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

**📝 Use When:
You want to show trends or changes over time. Great for line charts of stock prices, sales over months, etc.

**


---

## 📊 Bar Chart

```python
categories = ['A', 'B', 'C']
values = [5, 7, 3]

plt.bar(categories, values, color='orange')
plt.title("Bar Chart")
plt.xlabel("Category")
plt.ylabel("Values")
plt.show()
```

**📝 Use When:
You need to compare quantities across different categories. Useful for visualizing survey responses, product sales, etc.**


---


## 📉 Scatter Plot

```python
x = [1, 2, 3, 4, 5]
y = [5, 4, 3, 2, 1]

plt.scatter(x, y, color='red')
plt.title("Scatter Plot")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()
```

**📝 Use When:
You want to observe relationships or correlations between two numerical variables. Perfect for showing clusters or outliers.
**


---


## 🥧 Pie Chart

```python
labels = ['Apples', 'Bananas', 'Cherries']
sizes = [40, 30, 30]

plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140)
plt.axis('equal')  # Equal aspect ratio ensures a circle.
plt.title("Fruit Distribution")
plt.show()
```

**📝 Use When:
You need to show proportions of a whole — such as market share, expense distribution, etc.**

---

## 🔧 Customizing Plots

These are for improving readability, presentation, or saving your work. For example:

- Use plt.grid(True) to help see values better.
- Use plt.savefig() to export the plot as a PNG/JPG.


### 🔹 plt.xticks() and plt.yticks()
Customize or rotate axis tick labels.

```python
plt.xticks(rotation=45)
```
📌 Use When: Labels are overlapping or hard to read.

### 🔹 plt.legend()
Adds a legend for identifying multiple plots.

```python
plt.plot(x1, y1, label="Line 1")
plt.plot(x2, y2, label="Line 2")
plt.legend()
```
📌 Use When: You have multiple lines or data series in one chart.

### 🔹 plt.style.use()

Apply predefined styles for visual appearance.
```python
plt.style.use('ggplot')  # or 'seaborn', 'bmh', 'dark_background'
```
📌 Use When: You want quick aesthetic improvements without manual styling.

### 🔹 plt.tight_layout()

Adjusts padding to prevent label overlapping.
```python
plt.tight_layout()
```

---

## 🔗 Resources

📘 [Matplotlib Tutorial – W3Schools](https://www.w3schools.com/python/matplotlib_intro.asp)  
📘 [Matplotlib Documentation (Official)](https://matplotlib.org/stable/contents.html)  
📘 [Matplotlib Gallery (Examples)](https://matplotlib.org/stable/gallery/index.html)
