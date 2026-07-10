# 🚢 Titanic Survival Prediction — Logistic Regression

A machine learning project that predicts whether a passenger survived the Titanic disaster using **Logistic Regression**, built and trained on the classic Titanic dataset.

---

## 📌 Project Overview

The sinking of the Titanic is one of the most well-known maritime disasters, and the dataset associated with it is a classic starting point for classification problems in machine learning. This project builds a Logistic Regression model to predict passenger survival based on features like class, sex, age, fare, and more.

---

## 📂 Dataset

- **Source:** Titanic dataset (loaded via `seaborn.load_dataset("titanic")`)
- **Rows:** 891 passengers
- **Target variable:** `survived` (0 = Did not survive, 1 = Survived)

**Features used:**

| Feature    | Description                          |
|------------|---------------------------------------|
| pclass     | Passenger class (1st, 2nd, 3rd)      |
| sex        | Gender                               |
| age        | Age of passenger                     |
| sibsp      | # of siblings/spouses aboard         |
| parch      | # of parents/children aboard         |
| fare       | Ticket fare                          |
| embarked   | Port of embarkation                  |
| alone      | Whether passenger was traveling alone |

Dropped columns: `deck`, `embark_town`, `alive`, `who`, `adult_male`, `class` (redundant or high-missing-value features).

---

## 🛠️ Workflow

1. **Data Loading** — Loaded Titanic dataset from Seaborn.
2. **Data Cleaning**
   - Dropped redundant/high-null columns
   - Filled missing `age` values with the mean
   - Dropped rows with missing `embarked` values
3. **Encoding**
   - Label-encoded `sex` and `embarked` into numeric form
4. **Train/Test Split** — 80/20 split using `train_test_split`
5. **Model Training** — Logistic Regression (`sklearn.linear_model`)
6. **Model Evaluation**
   - Accuracy Score
   - Confusion Matrix
   - Classification Report (Precision, Recall, F1-score)
   - ROC Curve & AUC Score

---

## 📊 Results

| Metric              | Score   |
|----------------------|---------|
| **Accuracy**         | 80.3%   |
| **AUC Score**        | 0.797   |
| Precision (Survived) | 0.74    |
| Recall (Survived)    | 0.77    |
| F1-score (Survived)  | 0.75    |

**Confusion Matrix** and **ROC Curve** visualizations are included in the notebook to further illustrate model performance.

---

## 🧰 Tech Stack

- **Python 3**
- **Pandas** & **NumPy** — data manipulation
- **Matplotlib** & **Seaborn** — visualization
- **Scikit-learn** — model building & evaluation

---

## 🚀 How to Run

1. Clone this repository / download the notebook.
2. Open `Logistic_regression_project_Titanic_survival.ipynb` in **Google Colab** or **Jupyter Notebook**.
3. Run all cells in order — the Titanic dataset loads automatically via `seaborn.load_dataset()`, no external files needed.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 🔮 Future Improvements

- Try other classification models (Random Forest, XGBoost) for comparison
- Perform hyperparameter tuning (GridSearchCV)
- Feature engineering (title extraction from names, family size, fare binning)
- Handle class imbalance with techniques like SMOTE

---

## ✍️ Author

**Maroof**
BSCS Student | Transitioning into Data Science & AI

---

⭐ If you found this project useful, feel free to star the repo!
