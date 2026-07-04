# 📊 Formative 3: Probability Distributions, Bayesian Statistics & Gradient Descent
## Team Presentation Guide

**Team Members:**
- Saad - [GitHub Username]
- Towi - [GitHub Username]
- Diane - [GitHub Username]
- Esther - [GitHub Username]

**Presentation Date:** Tuesday, 7 July 2026  
**Time Slot:** [Time]  
**Total Duration:** 15 minutes

---

## 📋 Presentation Overview

| Part | Topic | Speaker | Duration |
|------|-------|---------|----------|
| Part 1 | EM Algorithm & Probability Distributions | [Name] | 3 min |
| Part 2 | Bayesian Probability | [Name] | 3 min |
| Part 3 & 4 | Gradient Descent (Manual & Code) | [Name] | 7 min |

---

# 🧬 PART 1: Expectation-Maximization (EM) Algorithm
### Speaker: [Member Name] | Time: 0-5 minutes

## 🎯 Objective
Cluster unlabeled height data from two populations (Parents vs. Children) using a mixture of Gaussian distributions.

## ❓ Critical Question: Why NOT Split at the Global Mean?

**Answer:** Splitting at the global mean is fundamentally flawed because:

1. **Ignores Variance:** It treats both distributions as having equal spread
2. **Misclassification Risk:** Points in the overlapping region get incorrectly assigned
3. **Hard Assignments:** Forces binary classification instead of probabilistic reasoning
4. **Suboptimal Parameters:** Doesn't account for the actual shape of each distribution

**Solution:** Use EM algorithm with **soft assignments** (probabilistic responsibilities)

## 📐 Mathematical Foundation

### Gaussian Probability Density Function

P(x|μ,σ²) = (1/√(2πσ²)) * exp(-(x-μ)²/(2σ²))


### EM Algorithm Steps

**E-Step (Expectation):**
γ(i,k) = π_k * P(x_i|μ_k,σ_k²) / Σ_j π_j * P(x_i|μ_j,σ_j²)


**M-Step (Maximization):**
μ_k = Σ_i γ(i,k) * x_i / Σ_i γ(i,k)
σ_k² = Σ_i γ(i,k) * (x_i - μ_k)² / Σ_i γ(i,k)
π_k = Σ_i γ(i,k) / N


## 💻 Implementation Code

### [MEMBER 1: INSERT YOUR CODE SNIPPETS HERE]

**Initialization:**
```python
# [INSERT YOUR INITIALIZATION CODE]

E-Step Function:

M-Step Function:

Main EM Loop:


python
1
📊 Optimization Tracking Table
Iteration
μ₁ (Children)
μ₂ (Parents)
σ₁²
σ₂²
π₁
π₂
Log-Likelihood
0
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
1
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
2
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
[Value]
🎲 LIVE DEMO: Posterior Probability Classification
Test Height: [Coach will provide during presentation]
[MEMBER 1: INSERT YOUR PREDICTION CODE]
python
1234567
Expected Output:
12
📈 Visualizations
Distribution Plot

[MEMBER 1: Add caption explaining what this shows]
Convergence Plot

[MEMBER 1: Add caption explaining convergence behavior]
🎬 PART 2: Bayesian Probability
Speaker: [Member Name] | Time: 5-10 minutes
🎯 Objective
Apply Bayes' Theorem to calculate sentiment probabilities from IMDb movie reviews using basic Python only (no ML libraries).
📝 Keyword Selection & Justification
[MEMBER 2: INSERT YOUR KEYWORD CHOICES AND JUSTIFICATION]
Positive Sentiment Keywords:
[Keyword 1] - Justification: [Why this indicates positive sentiment]
[Keyword 2] - Justification: [Why this indicates positive sentiment]
[Keyword 3] - Justification: [Why this indicates positive sentiment]
[Keyword 4] - Justification: [Why this indicates positive sentiment]
Negative Sentiment Keywords:
[Keyword 1] - Justification: [Why this indicates negative sentiment]
[Keyword 2] - Justification: [Why this indicates negative sentiment]
[Keyword 3] - Justification: [Why this indicates negative sentiment]
[Keyword 4] - Justification: [Why this indicates negative sentiment]
🧮 Bayes' Theorem
1
Components:
Prior: P(Positive) = Base probability of positive reviews
Likelihood: P(keyword|Positive) = Probability of keyword given positive review
Marginal: P(keyword) = Total probability of keyword across all reviews
Posterior: P(Positive|keyword) = Updated probability after seeing keyword
💻 Implementation Code
Data Preprocessing
[MEMBER 2: INSERT YOUR PREPROCESSING CODE]
python
1
Counting Keywords
[MEMBER 2: INSERT YOUR COUNTING CODE]
python
1
Bayes' Theorem Implementation
[MEMBER 2: INSERT YOUR BAYES CALCULATION CODE]
python
1
📊 Probability Results Tables
Positive Keywords Analysis
Keyword
Prior P(Pos)
Likelihood P(word|Pos)
Marginal P(word)
Posterior P(Pos|word)
[Word 1]
[Value]
[Value]
[Value]
[Value]
[Word 2]
[Value]
[Value]
[Value]
[Value]
[Word 3]
[Value]
[Value]
[Value]
[Value]
[Word 4]
[Value]
[Value]
[Value]
[Value]
Negative Keywords Analysis
Keyword
Prior P(Pos)
Likelihood P(word|Pos)
Marginal P(word)
Posterior P(Pos|word)
[Word 1]
[Value]
[Value]
[Value]
[Value]
[Word 2]
[Value]
[Value]
[Value]
[Value]
[Word 3]
[Value]
[Value]
[Value]
[Value]
[Word 4]
[Value]
[Value]
[Value]
[Value]
📈 Interpretation
[MEMBER 2: INSERT YOUR ANALYSIS]
[Explain what the posterior probabilities tell us about each keyword's predictive power]
📊 Visualization
[MEMBER 2: INSERT YOUR VISUALIZATION CODE]
python
1

[MEMBER 2: Add caption explaining the visualization]
🧮 PART 3 & 4: Gradient Descent
Speaker: [Member Name] | Time: 10-15 minutes
🎯 Objective
Implement gradient descent for linear regression using matrix operations, both manually (Part 3) and in Python with SciPy (Part 4).
📐 Problem Setup
Linear Equation:
1
Given Parameters:
Initial m = [-1, 2]
Initial b = [1, 1] (Note: Treated as vector, NOT scalar)
Data X = [[1, 3], [4, 10]]
Data y = [5, 6]
Learning Rate (α) = 0.001
Iterations = [Number of group members]
📝 Part 3: Manual Calculation
Cost Function: Mean Squared Error (MSE)
12
Chain Rule Derivatives
[MEMBER 3: INSERT YOUR DERIVATION STEPS]
Derivative with respect to m:
1
Derivative with respect to b:
1
Manual Iteration Results
[MEMBER 3: INSERT YOUR STEP-BY-STEP CALCULATIONS]
Iteration 1:
123456
Iteration 2:
1
Iteration 3:
1
💻 Part 4: Python Implementation
Setup
python
12345678910111213141516
MSE Equation Function
[MEMBER 3: INSERT YOUR MSE FUNCTION]
python
1
Gradient Computation with SciPy
[MEMBER 3: INSERT YOUR GRADIENT CODE]
python
1
Training Loop
[MEMBER 3: INSERT YOUR TRAINING LOOP]
python
1
Sample Output
1234567891011
📊 Results & Analysis
Final Parameters
12345
📈 Trend Observations
[MEMBER 3: INSERT YOUR TREND ANALYSIS]
Key Observations:
✅ MSE consistently decreases with each iteration
✅ Parameters update in opposite direction of gradients
✅ Algorithm successfully minimizes error
✅ Matrix operations maintained throughout (no scalar shortcuts)
📉 Visualizations
Parameter Trajectory
[MEMBER 3: INSERT YOUR PLOTTING CODE]
python
1

[MEMBER 3: Add caption explaining parameter convergence]
Error Convergence
[MEMBER 3: INSERT YOUR MSE PLOTTING CODE]
python
1

[MEMBER 3: Add caption explaining error reduction]
🎤 Q&A Preparation
Potential Questions by Part
Part 1 (EM Algorithm)
Why use soft assignments instead of hard assignments?
How does the algorithm know when to stop?
What happens if initialization is poor?
Part 2 (Bayesian)
Why choose these specific keywords?
How does the prior affect the posterior?
What are the limitations of this approach?
Part 3 & 4 (Gradient Descent)
Why is the learning rate important?
What happens if learning rate is too high/low?
Why use matrix operations instead of scalars?
📁 Repository Structure
