# 📘 Machine Learning Theory Assignment 1

## 📍 Overview
This repository contains the implementation and report for **Machine Learning Assignment 1**  
as part of the course *ICS1502 – Introduction to Machine Learning* at  
**Sri Sivasubramaniya Nadar College of Engineering**.

The assignment focuses on applying **linear regression** and **logistic regression** techniques  
using matrix-based methods and analyzing the effects of **regularization**, **normalization**, and **outliers**.

---

## 🧠 Part A – Mobile Phone Price Prediction (Regression)

### 🎯 Objective
To predict mobile phone prices using Linear Regression and evaluate:
- Closed-form solution (Normal Equation)
- Gradient Descent method
- Ridge Regression (L2 Regularization)
- Effect of Standardization on model accuracy

### 🧮 Methods Used
1. **Closed-Form Solution:**  
   \[
   \theta = (X^TX)^{-1}X^Ty
   \]

2. **Gradient Descent:**  
   Iterative weight updates with a chosen learning rate.

3. **Ridge Regression:**  
   Adds regularization term to control overfitting:  
   \[
   \theta = (X^TX + \lambda I)^{-1}X^Ty
   \]

### 📊 Results Summary
| Method | Regularization | Standardization | RMSE | R² |
|---------|----------------|-----------------|------|----|
| Closed-form | No | Yes | 205.6 | 0.89 |
| Gradient Descent | No | Yes | 206.2 | 0.88 |
| Ridge (λ=1) | Yes | No | 210.7 | 0.87 |
| Ridge (λ=1) | Yes | Yes | 198.3 | 0.91 |

### 🖼️ Visual Outputs
- Predicted vs Actual Price Plot  
- RMSE comparison  
- Effect of regularization on predictions  

---

## 🧠 Part B – Bank Note Authentication (Classification)

### 🎯 Objective
To classify bank notes as **genuine or forged** using Logistic Regression  
and evaluate its performance with and without L2 regularization.

### 🧮 Mathematical Model
\[
P(y=1|x) = \frac{1}{1 + e^{-X\theta}}
\]

### 🔍 Tasks Performed
1. Train/test split (80:20)
2. Logistic regression without regularization
3. Logistic regression with L2 regularization
4. Accuracy vs λ plot
5. 3D visualization using top 3 important features
6. Inject outliers and re-evaluate model robustness

### 📊 Results Summary
| Model | Regularization | Accuracy |
|--------|----------------|-----------|
| Logistic Regression | None | 0.975 |
| Logistic Regression (L2) | Yes | 0.978 |
| After Outlier Injection | L2 | 0.961 |

### 🧩 Feature Importance
Top features based on L2 weights:
- Variance  
- Curtosis  
- Entropy  
- Skewness  

---

## 🧰 Libraries Used
| Library | Purpose |
|----------|----------|
| **NumPy** | Matrix and vector operations |
| **Pandas** | Data loading and cleaning |
| **Matplotlib** | Visualizations and plots |
| **Scikit-learn** | Model training, scaling, metrics |
| **mpl\_toolkits.mplot3d** | 3D visualization of features |

---

## 🧾 Datasets

| Dataset | Description | Source |
|----------|--------------|--------|
| **Cellphone.csv** | Mobile specification dataset used for regression | Local (Drive) |
| **BankNote_Authentication.csv** | Bank note authentication data (Variance, Skewness, Curtosis, Entropy, Class) | [Kaggle – Bank Note Authentication Dataset](https://www.kaggle.com/datasets/ritesaluja/bank-note-authentication-uci-data) |

🧠 Key Learnings

Understood linear models using matrix formulations.

Observed the effect of normalization and regularization on performance.

Learned how outliers affect classification boundaries.

Practiced implementing regression and classification from scratch using NumPy and Scikit-learn.

🏁 Conclusion

This assignment helped in strengthening the understanding of fundamental machine learning concepts such as regression, classification, and regularization.
Even simple linear models performed strongly when features were standardized and regularized properly.
The project also emphasized that model performance heavily depends on proper data preprocessing rather than just algorithm complexity.

Prepared by: Harini J
M.Tech CSE (Integrated)*
Sri Sivasubramaniya Nadar College of Engineering
   git clone https://github.com/harriinnii/ML-TheoryAssignment1.git
   cd ML-TheoryAssignment1
