## Population vs Sample

- **Population**: The entire group you want to draw conclusions about.  
  Example: All people living in India.

- **Sample**: A subset of the population selected for analysis.  
  Example: 1,000 randomly selected people from India.

---

## Central Limit Theorem (CLT)

The Central Limit Theorem says that as the sample size increases (typically n ≥ 30), the distribution of the sample mean approaches a normal distribution — even if the population is not normal.

### Key Points:
- Mean of the sample means ≈ population mean  
  μₓ̄ = μ

- Standard deviation of the sample means (standard error):  
  σₓ̄ = σ / √n

### Why It Matters:
- Allows use of normal distribution tools
- Enables construction of confidence intervals
- Supports hypothesis testing

### Example:
If you repeatedly take random samples of 100 students and calculate their average height, those averages will form a bell-shaped curve — even if individual heights are not normally distributed.


---

## 📌 Confidence Intervals

### ✅ Definition
A **confidence interval** gives a range of values that is likely to contain the population parameter (like mean or proportion) with a certain level of confidence (e.g., 95%).

---

### ✅ Interpretation
A 95% confidence interval means **we are 95% confident that the true population parameter lies within this interval**.

---

### ✅ Formula (Population Mean, Known σ)

CI = x̄ ± Z * (σ / √n)

- `x̄`: sample mean  
- `Z`: Z-score (e.g., 1.96 for 95% confidence)  
- `σ`: population standard deviation  
- `n`: sample size


---

### ✅ Formula (Population Mean, Unknown σ)
CI = x̄ ± t * (s / √n)


- `t`: t-score (based on degrees of freedom)  
- `s`: sample standard deviation

---

### ✅ Example

Suppose:
- Sample mean height = 170 cm  
- Sample standard deviation (s) = 10 cm  
- Sample size (n) = 100  
- Confidence level = 95% → Z = 1.96

CI = 170 ± 1.96 * (10 / √100)
= 170 ± 1.96
= (168.04 cm, 171.96 cm)


We are 95% confident that the average height of the population lies between **168.04 cm and 171.96 cm**.

