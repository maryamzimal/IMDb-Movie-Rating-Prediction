# IMDb Movie Rating Prediction

## 📌 Project Overview

This project focuses on **predicting IMDb movie ratings** for Indian movies using **machine learning**. A **Random Forest Regressor** is trained on numerical features extracted and cleaned from the dataset.
---


The goal is to understand how factors like **release year, movie duration, and number of votes** influence IMDb ratings.
## 📂 Dataset

* **Source:** IMDb Movies India Dataset
* **Total Rows:** 15,509
* **Total Columns:** 10

### Columns Used

| Column   | Description                   |
| -------- | ----------------------------- |
| Year     | Movie release year            |
| Duration | Movie length in minutes       |
| Votes    | Number of IMDb votes          |
| Rating   | IMDb rating (target variable) |

---

## 🧹 Data Cleaning & Preprocessing

The dataset required significant preprocessing:

### 1️⃣ Handling Text Columns

* **Year:** `(2019)` → `2019`
* **Duration:** `109 min` → `109`
* **Votes:** `1,234` → `1234`

### 2️⃣ Missing Values

* Rows with missing **Rating** were removed
* Missing values in **Year, Duration, Votes** were filled using **median values**

### 3️⃣ Final Features

```python
X = ['Year', 'Duration', 'Votes']
y = 'Rating'
```
---
## 🤖 Model Used

* **Algorithm:** Random Forest Regressor
* **Library:** Scikit-learn

### Model Configuration

```python
RandomForestRegressor(
    n_estimators=200,
    random_state=42,
    n_jobs=-1
)
```



## 📊 Model Evaluation

The dataset was split as:

* **Training set:** 80%
* **Testing set:** 20%

### Evaluation Metrics

| Metric   | Score                                 |
| -------- | ------------------------------------- |
| MAE      | 0.93                                  |
| RMSE     | ~0.94                                 |
| R² Score | Indicates reasonable predictive power |

### Visualization

* Scatter plot of **Actual vs Predicted Ratings** was used to visually evaluate performance

---

## 📌 Future Improvements

* Feature engineering with categorical variables
* Model comparison (XGBoost, Linear Regression)
* Cross-validation
* Deploy as a web app

```
```
