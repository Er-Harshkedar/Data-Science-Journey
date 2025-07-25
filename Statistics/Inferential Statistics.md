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



---


## 📌 Hypothesis Testing

### ✅ Definition
**Hypothesis Testing** is a statistical method used to make decisions or inferences about a population based on sample data.

---

### ✅ Key Terminologies

- **Null Hypothesis (H₀):**  
  A statement that there is no effect or no difference.  
  Example: "The average salary of employees is ₹50,000."

- **Alternative Hypothesis (H₁):**  
  A statement that contradicts the null.  
  Example: "The average salary is not ₹50,000."

- **Significance Level (α):**  
  The probability of rejecting the null hypothesis when it is true. Common values are 0.05, 0.01.

- **P-value:**  
  The probability of obtaining results at least as extreme as the observed results, assuming H₀ is true.

---

### ✅ Types of Tests

1. **Z-test**:  
   Used when population variance is known and sample size is large.

2. **T-test**:  
   Used when population variance is unknown and sample size is small.

3. **Chi-square test**:  
   Used for categorical data to assess goodness-of-fit or independence.

4. **ANOVA (Analysis of Variance)**:  
   Used to compare means of three or more groups.

---

### ✅ Steps in Hypothesis Testing

1. State the null and alternative hypotheses.
2. Choose the significance level (α).
3. Select the appropriate test and calculate the test statistic.
4. Find the critical value or p-value.
5. Make a decision:  
   - If p-value ≤ α → Reject H₀  
   - If p-value > α → Fail to reject H₀

---

### ✅ Example

You want to test if the average delivery time of a food service is 30 minutes.

- H₀: μ = 30  
- H₁: μ ≠ 30  
- Sample mean = 28, s = 4, n = 25  
- Use t-test since σ unknown and n < 30



