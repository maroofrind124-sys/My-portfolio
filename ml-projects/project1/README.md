# 🏡 Boston Housing Price Prediction — Linear Regression

A machine learning project that predicts house prices in Boston using **Linear Regression**, with a strong focus on exploratory data analysis and feature engineering.

---

## 📌 Project Overview

This project uses the classic Boston Housing dataset to build a regression model that predicts median home values (`medv`) based on various neighborhood and housing characteristics. Beyond just fitting a model, the project emphasizes proper EDA, data cleaning, and feature engineering to improve prediction quality.

---

## 📂 Dataset

- **Source:** `BostonHousing.csv`
- **Target variable:** `medv` (Median value of owner-occupied homes, in $1000s)

**Key original features:**

| Feature   | Description                                   |
|-----------|------------------------------------------------|
| crim      | Per capita crime rate by town                 |
| zn        | Proportion of residential land zoned          |
| indus     | Proportion of non-retail business acres       |
| chas      | Charles River dummy variable (1 = bounds river) |
| nox       | Nitric oxide concentration                    |
| rm        | Average number of rooms per dwelling          |
| age       | Proportion of owner-occupied units built pre-1940 |
| dis       | Distance to employment centers                |
| rad       | Accessibility to radial highways              |
| tax       | Property tax rate                             |
| ptratio   | Pupil-teacher ratio by town                   |
| lstat     | % lower status of the population              |

---

## 🛠️ Workflow

1. **Exploratory Data Analysis (EDA)**
   - Distribution plots for all numeric features
   - Scatter plots (rooms vs price, lower status % vs price, crime vs price, tax vs price)
   - Boxplots for categorical/ordinal features vs price
   - Correlation heatmap
2. **Data Cleaning**
   - Removed duplicate rows
   - Filled missing `rm` values with median
3. **Feature Engineering**
   - Log transforms: `lstat_log`, `crim_log`, `dis_log` (to reduce skewness)
   - Polynomial feature: `rm_squared`
   - Custom ratio: `tax_per_rad`
   - Binned `age` into categories (new, recent, mid, old, very_old) with one-hot encoding
4. **Multicollinearity Check**
   - Feature-to-feature correlation heatmap to detect and manage redundant features
5. **Feature Selection**
   - Selected final feature set based on correlation with target and multicollinearity results
6. **Model Building**
   - Train/test split (80/20)
   - Standard scaling of numeric features
   - Linear Regression (`sklearn.linear_model`)
7. **Model Evaluation**
   - R² Score, Adjusted R², MAE, RMSE
   - Predicted vs Actual price visualization

---

## 📊 Results

| Metric                | Score  |
|-------------------------|--------|
| **R² Score**            | 0.77   |
| **Adjusted R²**         | 0.73   |
| **MAE** (Mean Absolute Error) | 2.79   |
| **RMSE** (Root Mean Squared Error) | 4.14   |

A **Predicted vs. Actual Price** scatter plot is included in the notebook to visually assess model performance.

---

## 🧰 Tech Stack

- **Python 3**
- **Pandas** & **NumPy** — data manipulation
- **Matplotlib** & **Seaborn** — visualization
- **Scikit-learn** — preprocessing, model building & evaluation

---

## 🚀 How to Run

1. Clone this repository / download the notebook and `BostonHousing.csv`.
2. Open `House_pricing_prediction_linear_regression.ipynb` in **Google Colab** or **Jupyter Notebook**.
3. Upload `BostonHousing.csv` when prompted (if running in Colab).
4. Run all cells in order.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 🔮 Future Improvements

- Try regularized regression models (Ridge, Lasso) to handle multicollinearity
- Experiment with tree-based models (Random Forest, Gradient Boosting) for comparison
- Perform hyperparameter tuning and cross-validation
- Add residual analysis to check regression assumptions

---

## ✍️ Author

**Maroof**
BSCS Student | Transitioning into Data Science & AI

---

⭐ If you found this project useful, feel free to star the repo!
