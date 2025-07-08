# Types of Probability Distributions

Probability distributions fall into two major categories: **Discrete** and **Continuous**.


## Key Differences

| Feature               | Discrete Distribution         | Continuous Distribution            |
|-----------------------|-------------------------------|-------------------------------------|
| Values                | Countable (0, 1, 2, …)        | Infinite/uncountable (real numbers) |
| Probability of single value | Non-zero (e.g., P(X=2) = 0.2) | Always zero (P(X=2) = 0)           |
| Represented by        | Probability Mass Function (PMF) | Probability Density Function (PDF) |
| Examples              | Binomial, Poisson             | Normal, Exponential, Uniform        |


---

# 📊 Discrete Uniform Distribution

## What is a Discrete Uniform Distribution?

A **Discrete Uniform Distribution** is a probability distribution where **each outcome in a finite set of possible outcomes is equally likely**. That is, if there are `n` possible outcomes, each outcome has a probability of `1/n`.

This is one of the simplest probability distributions and is often used in theoretical studies or in games of chance.

---

## 🎯 Characteristics

- Each outcome is **equally likely**.
- The set of outcomes is **finite and countable**.
- The probability mass function (PMF) is constant over all values.

---

## 📘 Probability Mass Function (PMF)

For a discrete uniform distribution with values:

\[
x_1, x_2, x_3, ..., x_n
\]

The PMF is:

P(X = xi) = 1 / n for i = 1, 2, ..., n
---

## 🧮 Example

**Rolling a fair 6-sided die**

Possible outcomes: {1, 2, 3, 4, 5, 6}  
Each number has an equal chance of appearing:

P(X = x) = 1 / 6 for x = 1 to 6

---

## 📏 Mean and Variance

For a discrete uniform distribution with values \( a, a+1, ..., b \):

- **Mean**:
  
  μ = (a + b) / 2

- **Variance**:  

  σ² = [(b - a + 1)^2 - 1] / 12
  
---

## 🧠 Applications

- Games of chance (dice, cards)
- Random selection from a fixed list
- Simulation and modeling of equally likely events

---

## ✅ Summary

- Discrete uniform distribution is simple but powerful.
- All outcomes are equally likely.
- Easy to compute probabilities, mean, and variance.

---


# Binomial Distribution

The **Binomial Distribution** models the number of successes in a fixed number of independent **Bernoulli trials**, each with the same probability of success.

---

## Characteristics

- Fixed number of trials: \( n \)
- Only two outcomes per trial: success or failure
- Probability of success on a single trial: \( p \)
- Probability of failure: \( 1 - p \)
- Trials are independent

---

## Probability Mass Function (PMF)

\[
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}
\]

Where:
- \( n \): total number of trials  
- \( k \): number of successes  
- \( p \): probability of success  
- \( \binom{n}{k} \): number of ways to choose \( k \) successes from \( n \) trials

---

## Mean and Variance

- **Mean (Expected Value)**:  
  \[
  E[X] = np
  \]

- **Variance**:  
  \[
  Var(X) = np(1 - p)
  \]

---

## Example

If we flip a coin 10 times and the probability of heads is 0.5, what is the probability of getting exactly 6 heads?

\[
P(X = 6) = \binom{10}{6} (0.5)^6 (0.5)^4 = \binom{10}{6} (0.5)^{10} = 210 \times \frac{1}{1024} \approx 0.205
\]

---

## Applications

- Modeling number of positive responses in surveys
- Predicting number of successful transactions or conversions
- Quality control in manufacturing (defective vs non-defective items)
- A/B testing in digital marketing



---


# Geometric Distribution

**Definition:**  
The geometric distribution models the number of trials needed to get the first success in a series of independent Bernoulli trials (yes/no experiments), each with the same probability of success \( p \).


## Probability Mass Function (PMF)

\[
P(X = k) = (1 - p)^{k-1} \cdot p
\]

Where:  
- \( X \) = the trial on which the first success occurs  
- \( k \) = trial number (1, 2, 3, ...)  
- \( p \) = probability of success on each trial  
- \( (1 - p) \) = probability of failure

---

## Properties

- The distribution is **memoryless**, meaning the probability of success in future trials does not depend on past failures.
- Mean (Expected value):  
\[
E(X) = 1/p
\]
- Variance:  
\[
Var(X) = 1 - p/p^2
\]

---

## Example

If the probability of success \( p = 0.2 \) in each trial, what is the probability that the first success occurs on the 3rd trial?

\[
P(X = 3) = (1 - 0.2)^{3-1} \times 0.2 = (0.8)^2 \times 0.2 = 0.128
\]




## Applications

- Modeling number of positive responses in surveys
- Predicting number of successful transactions or conversions
- Quality control in manufacturing (defective vs non-defective items)
- A/B testing in digital marketing

  
---

# Poisson Distribution

The **Poisson Distribution** is a discrete probability distribution that expresses the probability of a given number of events occurring in a **fixed interval of time or space**, assuming these events occur with a known constant rate and **independently** of the time since the last event.


## 📘 Probability Mass Function (PMF)

**P(X = k) = (λ^k * e^(-λ)) / k!**


Where:
- `X`: Number of occurrences (events)
- `λ` (lambda): Average rate (mean number of events in a time/space unit)
- `e`: Euler’s number (~2.718)
- `k`: Actual number of events (k = 0, 1, 2, ...)

---

## 🧮 Example

Suppose a website gets on average 3 user queries per minute. What is the probability of getting exactly 5 queries in a given minute?

λ = 3, k = 5
P(X = 5) = (3^5 * e^(-3)) / 5! = (243 * e^(-3)) / 120 ≈ 0.1008

## 🧠 Applications

- Modeling number of phone calls at a call center
- Number of decay events from a radioactive source
- Number of customer arrivals at a store per hour
- Defects per unit area in quality control


## ✅ Conditions to Use Poisson Distribution

- Events occur independently
- Events occur at a constant average rate
- Two events cannot occur at the exact same instant
- Probability of more than one event in an infinitesimally small time interval is negligible


---


## 2. 📗 Continuous Distributions

These apply when the random variable can take on **any value within a range** (i.e., infinitely many possible values).

### Examples:
- **Normal Distribution** (Gaussian): Bell-shaped curve
- **Exponential Distribution**: Time between events
- **Uniform Continuous Distribution**: Equal probability over an interval



# Normal Distribution (Gaussian)

The **Normal Distribution** is a continuous probability distribution that is **symmetrical** and shaped like a **bell curve**. It is one of the most widely used distributions in statistics and machine learning.

---

## 📘 Probability Density Function (PDF)

**f(x) = (1 / (σ * √(2π))) * e^(-(x - μ)² / (2σ²))**


Where:
- `μ` = mean (center of the distribution)
- `σ` = standard deviation (controls the spread)
- `x` = variable
- `e` = Euler’s number (~2.718)

---

## 🔍 Properties

- Symmetrical about the mean
- Mean = Median = Mode
- Total area under the curve = 1
- Defined for all real numbers: `x ∈ (−∞, ∞)`
- 68-95-99.7 Rule:
  - 68% data within 1σ
  - 95% data within 2σ
  - 99.7% data within 3σ


## 🧮 Example

If the heights of people are normally distributed with:

- `μ = 170 cm`, `σ = 10 cm`

Then the probability of someone being between 160 and 180 cm can be computed using the **Z-score** and normal tables or tools like SciPy.


## 📈 Applications

- Modeling natural phenomena (height, weight, IQ)
- Central Limit Theorem (CLT)
- Error terms in regression
- Assumptions in many statistical tests (t-test, ANOVA, etc.)


---


# Exponential Distribution

The **Exponential Distribution** is a continuous probability distribution used to model the **time between events** in a Poisson process (i.e., events that happen independently at a constant average rate).


## 📘 Probability Density Function (PDF)

**f(x; λ) = λ * e^(-λx), for x ≥ 0**

Where:
- `λ` is the rate parameter (λ > 0)
- `x` is the time between events
- `e` is Euler’s number (~2.718)

## 🔍 Properties

- Defined only for non-negative values: `x ≥ 0`
- Mean (Expected value):
E[X] = 1 / λ

- Variance:  
Var(X) = 1 / λ²

- Memoryless Property:  
The exponential distribution is the only continuous distribution that is **memoryless**, meaning:  
P(X > s + t | X > s) = P(X > t)



## 🧮 Example

Let’s say calls come into a call center at an average rate of 3 per hour (λ = 3).

Then the probability that the next call arrives in more than 10 minutes (i.e., `x > 1/6 hour`) is:

P(X > 1/6) = e^(-3 * 1/6) = e^(-0.5) ≈ 0.6065


## 📈 Applications

- Time between arrivals in queueing systems (e.g., customer service, web requests)
- Time until failure of an electronic device
- Lifetimes of radioactive atoms
- Modeling waiting times between independent events


---


# Continuous Uniform Distribution

The **Continuous Uniform Distribution** describes a situation where **all outcomes in a given interval are equally likely**. It is the continuous counterpart of the discrete uniform distribution.


## 📘 Probability Density Function (PDF)

For a uniform distribution between `a` and `b`:

f(x) = 1 / (b - a), for a ≤ x ≤ b

Outside the interval `[a, b]`, the probability is 0.

## 🔍 Properties

- **Mean**:
E[X] = (a + b) / 2


- **Variance**:  
Var(X) = (b - a)² / 12

- The probability is spread **evenly** across the interval
- The graph of the PDF is a horizontal line


## 🧮 Example

Suppose a bus arrives at a random time between 10:00 AM and 10:30 AM.  
Let `X ~ U(0, 30)` (in minutes).

- The probability the bus arrives between 10 and 10:10 (i.e., `X ≤ 10`) is:
P(X ≤ 10) = (10 - 0) / (30 - 0) = 1/3

## 📈 Applications

- Random number generation
- Simulation
- Modeling waiting times with no bias or pattern
- When you know the minimum and maximum but nothing else about distribution

