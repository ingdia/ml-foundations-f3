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
# [INSERT YOUR INITIALIZATION CODE]

E-Step Function:
<img width="620" height="86" alt="image" src="https://github.com/user-attachments/assets/493a994a-c87d-4b31-af93-963f48f9dab0" />

M-Step Function:
# [INSERT YOUR M-STEP CODE]
Main EM Loop:
# [INSERT YOUR MAIN LOOP CODE]



