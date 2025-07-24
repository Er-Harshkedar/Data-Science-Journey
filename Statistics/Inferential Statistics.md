## 🧑‍🤝‍🧑 Population vs Sample

In statistics, we often cannot study every individual in a group, so we work with a **sample**.

- **Population**: The entire group you want to draw conclusions about.  
  _Example_: All people living in India.

- **Sample**: A subset of the population selected for analysis.  
  _Example_: 1,000 randomly selected people from different states in India.

### Why Use a Sample?
- Studying an entire population can be **costly** and **time-consuming**.
- A **representative sample** allows us to make **inferences** about the population.

---

## 📊 Central Limit Theorem (CLT)

The **Central Limit Theorem** (CLT) is a fundamental concept in inferential statistics.

### Definition:
The CLT states that **the distribution of the sample means approaches a normal distribution**, as the sample size becomes large (typically n ≥ 30), **regardless of the original population distribution**.

### Key Points:
- Works even if the population is not normally distributed.
- The mean of the sample means equals the population mean:  
  \[
  \mu_{\bar{x}} = \mu
  \]
- The standard deviation of the sample means (standard error) is:  
  \[
  \sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
  \]

### Why It Matters:
CLT enables us to:
- Use **normal distribution tools** even for non-normal populations.
- Construct **confidence intervals**.
- Perform **hypothesis testing**.

### Example:
If you randomly select 100 students and record their heights, the **mean of their heights** will follow a normal distribution even if individual heights do not.

