#  Stock Market Data Analysis — Regression & Feature Engineering

###  Project Overview
This project explores factors that influence stock price behavior using regression-based techniques.
The analysis focuses on understanding how variables like **Volatility**, **Momentum**, **Dividend Yield**, and others relate to stock performance.
The goal is to develop a model that captures these relationships effectively using **Linear Regression**, **Ridge Regression**, and **Polynomial Regression**. The data is from Kaggle.

### Key Objectives
- Engineer meaningful features such as **Volatility** and **Momentum**.
- Apply **log-transformations** to handle skewed distributions.
- Compare performance between **Linear**, **Ridge**, and **Polynomial Regression**.
- Tune hyperparameters (e.g., `alpha`) using **GridSearchCV**.
- Select the best model based on **R²** and **MSE** performance metrics.

### Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn (optional for plots)
- Jupyter Notebook

### Feature Engineering
| Feature           | Description |
|-------------------|-------------|
| `Volatility`      | High Price - Low Price |
| `Momentum`        | (Close Price - Open Price) / Open Price |
| `LN(...)`         | Natural logarithm of several continuous variables |
| Polynomial Terms  | Degree-2 interactions for richer representation |

### Models Compared
| Model Type             | R² (Test Set) | Notes                        |
|------------------------|---------------|------------------------------|
| Linear Regression      | 0.7768        | Very strong baseline model   |
| Ridge Regression       | 0.7776        | Best model overall           |
| Lasso Regression       | 0.7749        | Slightly lower, still solid  |
| Polynomial Ridge (d=2) | 0.7540        | Slight improvement           |
| Polynomial Ridge (d=3) | -8.0          | Overfit 

### Final Model
**Ridge Regression (alpha = 1.0)**

- **R² = 0.7776** on test set
- Slightly outperforms both Linear and Lasso models.
- Regularization helps with stability and generalization.



### Acknowledgements
This project was built as part of my portfolio to demonstrate real-world data analysis and modeling skills in Python.