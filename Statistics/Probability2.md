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


