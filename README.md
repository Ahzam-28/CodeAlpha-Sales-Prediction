# 📈 Sales Prediction using Python

> Predict product sales based on advertising spend across TV, Radio, and Newspaper channels using machine learning regression models.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📋 Project Overview

Businesses spend billions on advertising every year — but which channels actually drive sales? This project uses **regression modeling** to predict sales based on advertising budget allocation across three channels (TV, Radio, Newspaper) and quantifies which channel delivers the best return.

### 🎯 Objectives
- Analyze the relationship between advertising spend and product sales
- Perform exploratory data analysis (EDA) with visualizations
- Build and compare **6 regression models**
- Evaluate models using R², MAE, MSE, and RMSE
- Identify the **most influential advertising channel**
- Forecast sales for new advertising budget scenarios
- Provide **actionable business recommendations**

---

## 📊 Dataset

The **Advertising dataset** contains **200 markets** with the following columns:

| Column | Description | Unit |
|--------|-------------|------|
| `TV` | Advertising budget spent on TV | thousands of $ |
| `Radio` | Advertising budget spent on Radio | thousands of $ |
| `Newspaper` | Advertising budget spent on Newspaper | thousands of $ |
| `Sales` | Product sales | thousands of units |

**Source:** Classic Advertising dataset from *An Introduction to Statistical Learning* (James, Witten, Hastie, Tibshirani) — included as `Advertising.csv` in this repository.

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **Pandas** & **NumPy** — data manipulation
- **Matplotlib** & **Seaborn** — visualization
- **Scikit-learn** — machine learning models and evaluation
- **Jupyter Notebook** — interactive development

---

## 📁 Repository Structure

```
CodeAlpha_SalesPrediction/
│
├── CodeAlpha_Task4_SalesPrediction.ipynb   # Main notebook
├── Advertising.csv                         # Dataset
└── README.md                               # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### Run the notebook
```bash
git clone https://github.com/<your-username>/CodeAlpha_SalesPrediction.git
cd CodeAlpha_SalesPrediction
jupyter notebook CodeAlpha_Task4_SalesPrediction.ipynb
```

---

## 🔍 Workflow

1. **Data Loading & Exploration** — read the CSV, inspect structure, check for missing/duplicate values
2. **EDA** — distributions, scatter plots with regression lines, correlation heatmap, pairplot
3. **Preprocessing** — train/test split (80/20), feature scaling for linear models
4. **Model Training** — fit 6 regression algorithms (linear and non-linear)
5. **Model Evaluation** — compare using R², MAE, MSE, and RMSE
6. **Diagnostic Plots** — actual vs. predicted, residual analysis
7. **Feature Importance** — quantify each channel's contribution to sales
8. **Forecasting** — predict sales for custom advertising-budget scenarios
9. **Impact Analysis** — visualize how varying each channel's spend affects predicted sales
10. **Business Recommendations** — translate findings into actionable marketing advice

---

## 🤖 Models Compared

| Model | R² Score | RMSE | MAE |
|-------|:--------:|:----:|:---:|
| **Gradient Boosting** | **0.9152** 🏆 | **1.62** | **1.10** |
| Random Forest | 0.9100 | 1.67 | 1.16 |
| Lasso Regression | 0.8696 | 2.01 | 1.49 |
| Linear Regression | 0.8675 | 2.02 | 1.53 |
| Ridge Regression | 0.8671 | 2.02 | 1.52 |
| Decision Tree | 0.8157 | 2.38 | 1.64 |

> 🏆 **Best Model: Gradient Boosting Regressor** — explains **~92% of the variance** in sales.

---

## 📈 Key Findings

### Channel Impact (Feature Importance)
| Channel | Importance | Verdict |
|---------|:----------:|---------|
| 📺 **TV** | ~67% | 🟢 Strongest driver of sales |
| 📻 **Radio** | ~28% | 🟡 Solid runner-up |
| 📰 **Newspaper** | ~5% | 🔴 Negligible impact |

### Insights
- **TV advertising** is by far the most influential channel — every dollar spent has the highest expected return.
- **Radio** acts as a strong supplement to TV; combining both yields better results than TV alone.
- **Newspaper** spending shows almost no measurable impact on sales — that budget is largely wasted.
- The model captures **~92% of the variance** in sales, indicating advertising spend is the dominant predictor in this dataset.

---

## 💼 Business Recommendations

1. **🟢 Prioritize TV** — sustain or increase TV ad spend; it delivers the largest sales lift per dollar.
2. **🟢 Use Radio as a force-multiplier** — TV + Radio outperforms TV alone.
3. **🔴 Reduce or eliminate Newspaper spending** — redirect that budget to TV or Radio.
4. **📊 Use the trained model** to estimate ROI of proposed campaigns *before* committing budget.
5. **🔄 Re-train periodically** as new market data arrives to keep predictions current.

---

## 💡 Learning Outcomes

By completing this project I learned to:
- Apply the full regression workflow: **load → explore → preprocess → train → evaluate → forecast**
- Compare linear and non-linear regression algorithms
- Interpret regression coefficients and tree-based feature importance
- Diagnose model fit using residual plots
- Translate model output into **business recommendations**
- Build a reusable prediction function for what-if scenario analysis

---

## 🔮 Possible Extensions

- Add **interaction features** (e.g., TV × Radio) to capture synergy effects
- Tune hyperparameters with `GridSearchCV` or `RandomizedSearchCV`
- Incorporate **time-series components** (seasonality, holidays, trend) when temporal data is available
- Deploy the model as a **REST API** with Flask or FastAPI
- Build an interactive **Streamlit dashboard** for marketing teams

---

---

## 📜 License

This project is licensed under the MIT License — feel free to use it for learning purposes.

---

⭐ If you found this helpful, please consider giving the repo a star!
