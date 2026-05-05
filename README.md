# 📊 Multiple Linear Regression from Scratch (Matrix Form)

## 🧠 Overview

This project implements **Multiple Linear Regression from scratch** using the **Normal Equation (closed-form solution)** to build strong mathematical intuition behind how linear regression works internally.

The goal of this notebook is not to build a production model, but to deeply understand the mathematics behind regression and how libraries like `scikit-learn` internally solve the problem.

---

## 🎯 Objectives

- Understand linear regression from a mathematical perspective
- Implement the model without using sklearn's LinearRegression
- Learn how bias/intercept is handled using matrix augmentation
- Compare custom implementation with sklearn results
- Visualize regression as a geometric plane in 3D space

---

## 🧮 Mathematical Formulation

We use the Normal Equation:

\[
B = (X^T X)^{-1} X^T Y
\]

Where:
- \(X\) = input feature matrix (with bias column added)
- \(Y\) = target variable
- \(B\) = parameter vector (weights + bias)

---

## 🛠️ Implementation Details

### Custom Class: `multi_LinearRegression`

The model is implemented using NumPy:

- `fit(x_train, y_train)`  
  Computes optimal parameters using the Normal Equation

- `predict(x_test)`  
  Generates predictions using learned parameters

- `get_parameters()`  
  Returns learned weights and intercept

---

## 📦 Dataset

The dataset used contains:
- **House Age**
- **Distance to nearest MRT station**
- **House price per unit area (target)**

---

## 📊 Data Preprocessing

- Train-test split using `sklearn.model_selection`
- Feature scaling using `StandardScaler`
- Bias term added manually using a column of ones

---

## 📈 Visualization

A **3D regression plane visualization** is created using Plotly:

- Red points → Actual data
- Blue points → Predicted values
- Black lines → Residual errors (difference between actual and predicted values)
- Surface → Learned regression plane

This helps visualize how the model fits a hyperplane in feature space.

---

## 🔍 Model Evaluation

Performance is evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

The results are compared with `sklearn.linear_model.LinearRegression`.

---

## ✅ Key Result

The custom implementation produces **identical coefficients** to sklearn’s LinearRegression, confirming correctness of the implementation.

---

## 📌 Key Learnings

- Linear regression is a geometric plane fitting problem
- Bias can be treated as an additional feature
- Normal equation provides a closed-form solution
- Matrix operations are at the core of ML models
- Visualization improves intuition of model behavior

---

## 🚀 Future Improvements

- Implement Gradient Descent version of Linear Regression
- Add Ridge Regression (L2 regularization)
- Improve visualization (interactive sliders for weights)
- Add loss function visualization

---

## 🧑‍💻 Author

This project is part of an AI/ML learning journey focused on building machine learning models from scratch to strengthen mathematical intuition.

---

## ⭐ If you like this project

Feel free to star ⭐ the repository and follow the learning journey!
