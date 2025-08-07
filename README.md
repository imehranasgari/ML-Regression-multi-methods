# Bike Sharing Demand Prediction

## Problem Statement and Goal of Project

The objective of this project is to develop a machine learning model to **predict the hourly number of bike rentals** in a bike-sharing system based on various environmental and temporal features. This prediction helps in operational decision-making and resource optimization.

## Solution Approach

* **Exploratory Data Analysis (EDA):** Analyzed data structure and distributions; identified demand patterns based on season, weather, hour, etc.
* **Feature Engineering:** Converted `datetime` column into numerical features such as `hour`, `weekday`, and `month`.
* **Data Preparation:** Ensured alignment between train and test data; generated realistic random values for missing `casual` and `registered` columns in the test dataset based on training data statistics.
* **Modeling:** Implemented multiple regression models including `Decision Tree Regressor`, `Polynomial Regression`,`Random Forest Regression`,`KNN Regressor`, and `Multiple Linear Regression` to predict the target variable (`count`).
* **Prediction:** Used trained models to generate predictions on the test dataset and stored results in the `count` column.

## Technologies & Libraries

* **Python (Jupyter Notebook)**
* **pandas, numpy**
* **matplotlib, seaborn**
* **scikit-learn**

## Description About Dataset

* **Train Data:**

  * 10,886 rows
  * 12 columns including: datetime, season, holiday, workingday, weather, temp, atemp, humidity, windspeed, casual, registered, count
  * No missing values
  * `count`: target variable (continuous number of rentals)
* **Test Data:**

  * 6,493 rows
  * Similar structure to train data, but missing `casual` and `registered` (generated manually)
* **Features:**

  * `datetime` converted to `hour`, `weekday`, `month`
  * Categorical: season, weather, holiday, workingday
  * Environmental: temp, atemp, humidity, windspeed
  * Target: count

## Installation & Execution Guide

1. **Requirements:** Python 3.11.3, Jupyter Notebook
2. **Installation:**

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. **Execution:**

   * Place `train.csv` and `test.csv` in the same directory as the notebook
   * Run the notebook:

     ```bash
     jupyter notebook "Mini Project.ipynb"
     ```
   * Execute all cells in order to perform EDA, feature engineering, modeling, and prediction

## Key Results / Performance

* **EDA:** Identified interesting demand patterns across different seasons, weather conditions, and hours of the day.
* **Models:** Three regression models were implemented: Decision Tree Regressor, Polynomial Regression, and Multiple Linear Regression
* **Output:** Predictions from the Multiple Linear Regression model were selected as the final output and saved to the `count` column in the test dataframe
* **Performance Metrics:** No metrics such as RMSE or R² were reported (the focus was on completing the end-to-end prediction pipeline)

## Screenshots / Sample Outputs

**Sample prediction code:**

```python
df_test['count'] = Y_pred_multiple
df_test[['datetime', 'count']].head()
```

**Sample Output:**

| datetime            | count |
| ------------------- | ----- |
| 2011-01-20 00:00:00 | 129.9 |
| 2011-01-20 01:00:00 | 108.7 |
| ...                 | ...   |

## Additional Learnings

* Gained strong understanding of feature engineering by transforming `datetime` into meaningful numeric features (`hour`, `weekday`, `month`)
* Learned to handle missing features in test datasets by generating realistic values based on training statistics
* Maintained full alignment between train and test data structures — critical for successful modeling
* Practiced implementing and comparing multiple regression models in a real-world-like task
* Understood the value of proper data exploration and transformation, even when the project’s main goal is just prediction generation

---

## 👤 Author

**Mehran Asgari**
**Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
**GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.

