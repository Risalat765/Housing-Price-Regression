# ALML CA1: Housing Price Regression Analysis

**Author:** Risalat Masrafi  
**Admin No:** P2508290  

---

## Project Overview
This project focuses on building a predictive regression model to estimate **Housing Prices** based on various property features. By analyzing factors such as city location, house area, and renovation status, the project aims to identify the most significant drivers of property value and develop a model that outperforms simple baseline averages.

## Dataset Description
The analysis is conducted on `housing_price_data.csv`, which includes:
* **City:** The location of the property (e.g., Chicago, Denver, New York).
* **House Area (sqm):** The total living space.
* **No. of Bedrooms/Toilets:** Key property capacity metrics.
* **Stories:** The number of levels in the home.
* **Renovation Status:** Categorical status (Furnished, Semi-furnished, Unfurnished).
* **Price ($):** The target variable for prediction.

## Machine Learning Workflow
1. **Exploratory Data Analysis (EDA):** Identified strong correlations between `House Area`, `No. of Toilets`, and the final `Price`.
2. **Data Processing:**
    * **Encoding:** Applied One-Hot Encoding to categorical variables like `City` and `Renovation Status`.
    * **Scaling:** Used `StandardScaler` to normalize numerical features for regression.
3. **Model Comparison:** Evaluated several algorithms, including:
    * Linear Regression
    * Lasso Regression
    * Support Vector Regressor (SVR)
    * **Ridge Regression** (Selected as the best-performing model)
4. **Hyperparameter Tuning:** * Used `GridSearchCV` to optimize the Ridge `alpha` parameter.
    * Optimized alpha value: **24.01**.
5. **Evaluation:** Compared the final model against a **Dummy Regressor** baseline.

## Key Results
* **Baseline MAE:** 148,306.11
* **Cross-validated MAE:** 94,382.58
* **Final Test Set MAE:** **83,805.14**
* **Conclusion:** The tuned Ridge Regression model significantly reduced error compared to the baseline, proving the effectiveness of feature engineering and hyperparameter optimization for this dataset.

## Getting Started

### Prerequisites
Install the required Python libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn