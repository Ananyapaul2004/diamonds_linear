## Diamond Price Prediction: Regression Modeling 

This project involves data exploration and regression modeling to predict diamond prices using a tabular dataset. The objective is to clean the data, analyze relationships between features, and compare multiple regression models, including an investigation into how well regularization handles multicollinearity.

### Files

* `diamonds_eda_preprocessing_one hot encoded.ipynb` — Data loading, cleaning, EDA, and one-hot/ordinal encoding
* `codes_diamonds.ipynb` — Model training, hyperparameter tuning, and evaluation
* `diamonds_result.ipynb` — Final results, model comparison, and multicollinearity investigation
* `diamonds.csv` — Original (raw) dataset
* `Project_report_linear.pdf` — Full written project report

NOTE: The cleaned dataset is generated within the notebooks and is not stored separately in this repository.

---

### Features

* **EDA** using pandas, matplotlib, seaborn to examine price distribution, correlations, and outliers.
* **Data cleaning** using a ratio-based diagnostic to remove physically inconsistent measurements, while retaining rare-but-valid values.
* **Model training** using multiple regressors:

  * Linear Regression
  * Ridge Regression
  * Lasso Regression
  * Elastic Net
  * Random Forest
* **Hyperparameter tuning** using RidgeCV, LassoCV, ElasticNetCV, and RandomizedSearchCV.
* **Multicollinearity diagnosis** using Variance Inflation Factor (VIF).

---

### Results

Random Forest achieved the best performance (R² ≈ 0.982, RMSE ≈ $527). Linear, Ridge, and Elastic Net performed comparably (R² ≈ 0.95). A dedicated investigation found that regularization tuned for accuracy does not resolve the severe multicollinearity between carat and diamond dimensions (x, y, z); removing the redundant features directly was required to restore a physically correct coefficient for carat.

---
📌 Author

**Ananya Paul**
