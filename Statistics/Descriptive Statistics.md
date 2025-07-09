# Types of Data in Statistics

Understanding data types is essential in statistics and data science because it determines which analysis and visualizations are appropriate.

---

## 📘 1. Qualitative (Categorical) Data

These represent **categories or labels**. They describe *qualities* rather than quantities.

### 🔹 Types:
- **Nominal**: Categories with no order  
  → e.g., gender, colors, city names  
- **Ordinal**: Categories with a meaningful order  
  → e.g., survey ratings (bad, average, good), education level

---

## 📗 2. Quantitative (Numerical) Data

These represent **measurable quantities** and involve numbers.

### 🔹 Types:
- **Interval**: Numeric data **without a true zero point**  
  → e.g., temperature in Celsius, IQ score  
- **Ratio**: Numeric data **with a true zero point**  
  → e.g., height, weight, salary, age

---

## 📊 Summary Table

| Data Type   | Subtype   | Ordered? | Numeric? | Example                      |
|-------------|-----------|----------|----------|------------------------------|
| Categorical | Nominal   | ❌       | ❌       | Colors, Gender, Nationality  |
| Categorical | Ordinal   | ✅       | ❌       | Low/Medium/High, Rankings    |
| Numerical   | Interval  | ✅       | ✅       | Temperature (°C), Dates      |
| Numerical   | Ratio     | ✅       | ✅       | Age, Income, Distance        |

---

## 💡 Why This Matters

- **Statistical tests** depend on data type (e.g., chi-square for categorical, t-test for numerical)
- **Machine learning algorithms** treat numeric vs categorical features differently
- **Visualizations** vary based on data type (e.g., bar chart vs histogram)
