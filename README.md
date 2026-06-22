# 🏪 Big Mart Sales Prediction Model

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![XGBoost](https://img.shields.io/badge/XGBoost-Regression-red?style=flat-square)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellowgreen?style=flat-square&logo=scikit-learn)
![Supervised ML](https://img.shields.io/badge/ML-Supervised%20Regression-blueviolet?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

A machine learning project that predicts the **outlet sales of products** across Big Mart stores using regression techniques. By analyzing product attributes and store characteristics, this model helps retailers forecast revenue and optimize inventory and pricing strategies.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Model Performance](#-model-performance)
- [Technologies Used](#-technologies-used)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🔍 Overview

In the highly competitive retail industry, accurately forecasting product sales is critical for:

- 📦 **Inventory Management** — Avoid overstocking or stockouts
- 💰 **Revenue Forecasting** — Plan budgets and set growth targets
- 🏷️ **Pricing Strategy** — Understand price sensitivity across outlets
- 🏬 **Store Optimization** — Identify high-performing outlet types

This project builds an end-to-end **supervised regression pipeline** on the Big Mart Sales dataset — covering data cleaning, feature engineering, label encoding, and model training — to predict `Item_Outlet_Sales` for each product-store combination.

---

## 📊 Dataset

| Property | Details |
|---|---|
| **File** | `Big_Mart_Dataset.csv` |
| **Domain** | Retail / FMCG |
| **Task Type** | Supervised Regression |
| **Target Variable** | `Item_Outlet_Sales` |
| **Total Records** | ~8,523 rows |
| **Total Features** | 11 input features |

### Feature Description

| Feature | Type | Description |
|---|---|---|
| `Item_Identifier` | Categorical | Unique product ID |
| `Item_Weight` | Numerical | Weight of the product |
| `Item_Fat_Content` | Categorical | Low Fat / Regular |
| `Item_Visibility` | Numerical | Percentage of display area in store |
| `Item_Type` | Categorical | Product category (e.g., Dairy, Snacks) |
| `Item_MRP` | Numerical | Maximum Retail Price |
| `Outlet_Identifier` | Categorical | Unique store ID |
| `Outlet_Establishment_Year` | Numerical | Year the outlet was established |
| `Outlet_Size` | Categorical | Store size — Small / Medium / High |
| `Outlet_Location_Type` | Categorical | City tier — Tier 1 / Tier 2 / Tier 3 |
| `Outlet_Type` | Categorical | Grocery Store / Supermarket Type |
| `Item_Outlet_Sales` | **Target** | Sales of the product at that outlet |

---

## ✨ Features

- **Data Cleaning** — Handles missing values in `Item_Weight` and `Outlet_Size`
- **Feature Engineering** — Derives outlet age from establishment year; normalizes inconsistent categorical labels
- **Label Encoding** — Converts all categorical variables to numerical format
- **Exploratory Data Analysis (EDA)** — Distribution plots, correlation heatmaps, and sales analysis by outlet type
- **Model Training** — Trains an XGBoost Regressor on the processed data
- **Model Evaluation** — Reports R² Score and RMSE on both training and test sets

---

## 📁 Project Structure

```
Big_Mart_Sales_Prediction_Model/
│
├── Big_Mart_Sales_Prediction_Model.ipynb   # Main notebook with full ML pipeline
├── Big_Mart_Dataset.csv                    # Dataset
└── README.md                               # Project documentation
```

---

## ⚙️ Installation

### Prerequisites

Ensure **Python 3.8+** is installed. Clone the repository and set up your environment.

```bash
# Clone the repository
git clone https://github.com/AliRaza-Dev678/Big_Mart_Sales_Prediction_Model.git
cd Big_Mart_Sales_Prediction_Model
```

### Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost jupyter
```

> **Tip:** Use a virtual environment to avoid dependency conflicts:
> ```bash
> python -m venv venv
> source venv/bin/activate      # Linux/macOS
> venv\Scripts\activate         # Windows
> ```

---

## 🚀 Usage

1. Launch Jupyter Notebook:

```bash
jupyter notebook
```

2. Open `Big_Mart_Sales_Prediction_Model.ipynb` in your browser.

3. Run all cells sequentially (`Cell → Run All`) to execute the full pipeline.

### Pipeline Overview

```
Load Data
    ↓
Exploratory Data Analysis (EDA)
    ↓
Handle Missing Values
    ↓
Feature Engineering & Label Encoding
    ↓
Train / Test Split
    ↓
Model Training (XGBoost Regressor)
    ↓
Evaluate — R² Score & RMSE
    ↓
Predict on New Data
```

---

## 📈 Model Performance

The model is evaluated using standard regression metrics:

| Metric | Description |
|---|---|
| **R² Score** | Measures how well the model explains variance in sales (closer to 1 is better) |
| **RMSE** | Root Mean Squared Error — average prediction error in sales units |

> Exact scores are printed at the end of the notebook after running all cells.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **Jupyter Notebook** | Interactive development environment |
| **NumPy** | Numerical computation |
| **Pandas** | Data manipulation and preprocessing |
| **Matplotlib / Seaborn** | Data visualization and EDA |
| **scikit-learn** | Preprocessing, train/test split, evaluation metrics |
| **XGBoost** | Gradient boosting regression model |

---

## 🤝 Contributing

Contributions and improvements are welcome! To contribute:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add: your feature description"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

**Ideas for contributions:**
- Try alternative models (Random Forest, LightGBM, CatBoost)
- Add hyperparameter tuning with GridSearchCV or Optuna
- Build a Streamlit web app for interactive sales predictions
- Add cross-validation for more robust evaluation

---

## 📄 License

This project is licensed under the **MIT License** — free to use, modify, and distribute with proper attribution.

---

## 👨‍💻 Author

**Ali Raza**
- GitHub: [@AliRaza-Dev678](https://github.com/AliRaza-Dev678)

---

> 💡 **Business Insight:** Sales forecasting with machine learning helps retailers reduce inventory waste, prevent stockout-driven revenue loss, and make smarter data-driven decisions at scale — a key competitive advantage in modern retail.
