# 📚 Scikit-Learn Basics

`scikit-learn` is the most widely used machine learning library in Python.  
It provides tools for **data preprocessing, model building, evaluation, and tuning**.

---

## 🛠️ Installation

```bash
pip install scikit-learn
```

---


🧠 Why Use Scikit-Learn?
- Easy-to-use syntax for ML models
- Wide range of algorithms (supervised & unsupervised)
- Built-in dataset loaders
- Data preprocessing utilities
- Model evaluation tools

---


⚙️ Basic Workflow in Scikit-Learn

1. Import the required modules
2. Load or create the dataset
3. Split into training and testing sets
4. Choose and initialize a model
5. Train the model
6. Make predictions
7. Evaluate performance

---


📊 Built-in Datasets
Scikit-learn includes small datasets for quick testing:

```python
from sklearn.datasets import load_iris, load_boston

iris = load_iris()
print(iris.data[:5])  # Features
print(iris.target[:5])  # Labels
```
Common built-in datasets:

- load_iris() – Flower classification
- load_digits() – Handwritten digit recognition
- load_wine() – Wine classification
- load_boston() – Housing prices (deprecated in new versions)


---


📝 Example: Linear Regression Workflow
```python
# 1. Import libraries
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# 2. Sample dataset
data = {
    'Hours_Studied': [2.5, 5.1, 3.2, 8.5, 3.5, 1.5, 9.2],
    'Exam_Score': [21, 47, 27, 75, 30, 20, 88]
}
df = pd.DataFrame(data)

# 3. Split into X (features) and y (target)
X = df[['Hours_Studied']]
y = df['Exam_Score']

# 4. Train-test split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# 5. Initialize model
model = LinearRegression()

# 6. Train the model
model.fit(X_train, y_train)

# 7. Make predictions
y_pred = model.predict(X_test)

# 8. Evaluate
print("Mean Squared Error:", mean_squared_error(y_test, y_pred))
print("R² Score:", r2_score(y_test, y_pred))
```

---


🧼 Data Preprocessing Tools

```python
from sklearn.preprocessing import StandardScaler, LabelEncoder

# Feature scaling
scaler = StandardScaler()
scaled_data = scaler.fit_transform(X)

# Encoding categorical labels
encoder = LabelEncoder()
labels = encoder.fit_transform(['cat', 'dog', 'cat'])
```


---


📏 Model Evaluation
- Regression Metrics: MAE, MSE, RMSE, R²
- Classification Metrics: Accuracy, Precision, Recall, F1 Score, Confusion Matrix

```python
from sklearn.metrics import confusion_matrix

y_true = [1, 0, 1, 1, 0]
y_pred = [1, 0, 1, 0, 0]
print(confusion_matrix(y_true, y_pred))
```

---

## 🔗 Resources

📘 [Scikit-Learn Documentation](https://scikit-learn.org/stable/documentation.html)  
📘 [Scikit-Learn Tutorial – W3Schools](https://www.w3schools.com/python/python_ml_getting_started.asp)  
📘 [Machine Learning with Scikit-Learn – GeeksforGeeks](https://www.geeksforgeeks.org/scikit-learn/)

---


✅ Summary
scikit-learn is your main toolkit for implementing machine learning in Python.
You’ll use it in every ML topic in this repository for:

- Loading datasets
- Preprocessing
- Training & testing models
- Evaluating results
