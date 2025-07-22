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

---


# Measures of Central Tendency

**Measures of Central Tendency** help describe the "center" or "typical value" of a dataset. They summarize where most values in a distribution fall.

---

## 📘 1. Mean (Average)

The **mean** is the sum of all values divided by the total number of values.

### 🔹 Formula:

**Mean (μ or x̄) = (x₁ + x₂ + ... + xₙ) / n

or

Mean = Σxᵢ / n
**

### 🔹 Example:
If values are 4, 6, 8:
Mean = (4 + 6 + 8) / 3 = 6

---

## 📗 2. Median

The **median** is the middle value when data is ordered.

- If `n` is **odd**, it's the middle value  
- If `n` is **even**, it's the average of the two middle values

### 🔹 Example:
- Data: 2, 3, 6 → Median = 3  
- Data: 2, 3, 6, 8 → Median = (3 + 6)/2 = 4.5

> ✅ Use median when the data has **outliers or is skewed**

---

## 📙 3. Mode

The **mode** is the value(s) that appear **most frequently** in the data.

- Can be **no mode**, **one mode** (unimodal), or **multiple modes** (bimodal/multimodal)

### 🔹 Example:
- Data: 1, 2, 2, 3 → Mode = 2  
- Data: 1, 2, 3 → No mode

> ✅ Mode is useful for **categorical data** too

---

## 💡 Summary

| Measure | Use When...                          | Sensitive to Outliers? |
|---------|--------------------------------------|-------------------------|
| Mean    | Data is symmetric or normal          | ✅ Yes                  |
| Median  | Data is skewed or has outliers       | ❌ No                   |
| Mode    | Need most frequent or categorical    | ❌ No                   |

---

## 📈 Visual Example (Skewed Distributions)

- **Right-skewed (positive skew)**:  
  Mean > Median > Mode

- **Left-skewed (negative skew)**:  
  Mode > Median > Mean


---



# Measures of Dispersion

Measures of dispersion describe **how spread out the values** in a dataset are. While central tendency tells us the "center", dispersion tells us **how much the data varies**.

---

## 1. Range

The **range** is the difference between the maximum and minimum values.

**Formula:**

    Range = Max - Min

**Example:**

    Data: 5, 7, 10, 12 → Range = 12 - 5 = 7

---

## 2. Variance (σ²)

Variance measures the **average squared distance** from the mean.

**Formula (Population):**

    σ² = Σ(xᵢ - μ)² / N

**Formula (Sample):**

    s² = Σ(xᵢ - x̄)² / (n - 1)

> Use population formula when you have data for the entire group; use sample formula when working with a subset.

---

## 3. Standard Deviation (σ or s)

Standard deviation is the **square root of variance**. It tells you **how much data deviates from the mean** in original units.

**Formula:**

    σ = √(σ²)   or   s = √(s²)

**Interpretation:**
- A small standard deviation → data is close to the mean
- A large standard deviation → data is spread out

---

## 4. Interquartile Range (IQR)

IQR measures the range of the **middle 50% of the data**. It helps eliminate the effect of outliers.

**Formula:**

    IQR = Q3 - Q1

Where:
- Q1 = 25th percentile
- Q3 = 75th percentile

---

## Summary Table

| Measure        | Description                          | Sensitive to Outliers? |
|----------------|--------------------------------------|-------------------------|
| Range          | Max - Min                            | ✅ Yes                  |
| Variance       | Average squared deviation from mean  | ✅ Yes                  |
| Standard Dev.  | Spread in same units as data         | ✅ Yes                  |
| IQR            | Spread of middle 50%                 | ❌ No                   |

---

## Visual Tip

- **IQR** is used in **box plots**
- **Standard deviation** is used in **bell curves (normal distribution)**



# Skewness and Kurtosis

In statistics, **Skewness** and **Kurtosis** help us understand the *shape and characteristics* of a data distribution beyond basic metrics like mean and standard deviation.

---

## 📈 Skewness

Skewness tells us **about the symmetry** of a distribution.
- It tells us **whether the data is balanced** or **pulled** toward one side.
- A skewed distribution means one tail is longer or fatter than the other.
- It affects the relationship between **mean, median, and mode**.

### Types of Skewness:

1. **Positive Skew (Right-Skewed)**  
   - Tail is on the **right** side  
   - Mean > Median > Mode

2. **Negative Skew (Left-Skewed)**  
   - Tail is on the **left** side  
   - Mean < Median < Mode

3. **Zero Skew (Symmetrical)**  
   - Perfectly symmetrical (like a normal distribution)  
   - Mean = Median = Mode

### Formula (Sample Skewness):

    Skewness = [n / ((n-1)(n-2))] * Σ[(xᵢ - x̄)/s]³

Where:
- n = sample size
- x̄ = sample mean
- s = sample standard deviation

> In practice, libraries like `scipy.stats.skew()` or `pandas.Series.skew()` are used.

---

## 🔼 Kurtosis

Kurtosis tells us **how peaked or flat** a distribution is, compared to a normal distribution.
- It describes the **shape of the tails** and **sharpness of the peak** of a distribution.
- High kurtosis means more data in the tails and possibly more **outliers**.
- Low kurtosis means fewer outliers and a flatter distribution.

### Types of Kurtosis:

1. **Mesokurtic (Kurtosis = 3)**  
   - Normal distribution

2. **Leptokurtic (Kurtosis > 3)**  
   - Tall, narrow peak  
   - Heavy tails (more outliers)

3. **Platykurtic (Kurtosis < 3)**  
   - Flat-topped curve  
   - Light tails (fewer outliers)

### Formula (Sample Kurtosis):

    Kurtosis = [n(n+1) / ((n-1)(n-2)(n-3))] * Σ[(xᵢ - x̄)/s]^4 - [3(n-1)² / (n-2)(n-3)]

> Excess Kurtosis = Kurtosis - 3  
> Most libraries like `scipy.stats.kurtosis()` return **excess kurtosis** by default.

---

## Summary Table

| Measure   | Description                             | Normal Value |
|-----------|-----------------------------------------|--------------|
| Skewness  | Symmetry of distribution                | 0            |
| Kurtosis  | Peakedness or tail heaviness            | 3 (or 0 excess) |

---

## Quick Tip:

- Use **Skewness** to check if the mean is being dragged by outliers.
- Use **Kurtosis** to check the likelihood of **extreme values**.

---

## ✅ Pro Tip

Use Python libraries to calculate them:
```python
from scipy.stats import skew, kurtosis

skewness_value = skew(data)
kurtosis_value = kurtosis(data)  # by default, excess kurtosis
```


---


# 📊 Z-Score and Percentiles

---

## 1. Z-Score

A **Z-score** (also called a **standard score**) tells us how many **standard deviations** a data point is **from the mean**.

### 🔹 Formula:
Z = (X - μ) / σ


Where:  
- `X` = data point  
- `μ` = mean of the distribution  
- `σ` = standard deviation  

### 🔹 Interpretation:
- `Z = 0` → the value is exactly the mean  
- `Z > 0` → the value is above the mean  
- `Z < 0` → the value is below the mean  

### ✅ Example:
Suppose a test has a mean score of 70 and standard deviation of 10.  
A student scored 85.

Z = (85 - 70) / 10 = 1.5

👉 This means the score is **1.5 standard deviations above the mean**.

---

## 2. Percentiles and Quartiles

Percentiles divide the data into **100 equal parts**.  
Each percentile shows the value **below which a certain percentage** of observations fall.

### 🔹 Common Percentiles:
- **25th percentile** = Q1 (First Quartile)
- **50th percentile** = Median = Q2
- **75th percentile** = Q3 (Third Quartile)

### 🔹 Use Cases:
- Percentile scores in exams
- Identifying outliers
- Creating box plots

---

## 3. Interpreting Percentiles:

- If a student is at the **90th percentile**, it means they scored **better than 90%** of the class.
- If an income is at the **25th percentile**, it means 25% of incomes are **less than or equal to** that value.

---

## 💡 Quartiles Recap:

| Quartile | Percentile | Meaning                        |
|----------|------------|--------------------------------|
| Q1       | 25th       | Lower quartile                 |
| Q2       | 50th       | Median of the dataset          |
| Q3       | 75th       | Upper quartile                 |
| IQR      | Q3 - Q1    | Range of middle 50% of values  |

