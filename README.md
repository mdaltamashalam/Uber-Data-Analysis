# Uber-Data-Analysis

This project focuses on analyzing Uber ride data to uncover insights and build predictive models for pricing. We leverage exploratory data analysis (EDA), feature engineering, and multiple regression algorithms to determine the best-performing model for predicting Uber ride prices.

---

## 📌 Problem Statement

We analyze Uber ride data available in tabular format, applying machine learning algorithms and statistical techniques to:
- Understand the relationships between features such as date, time, and location.
- Identify the most important variables affecting ride prices.
- Help Uber enhance its services by highlighting influential factors in pricing strategy.

---

## 🧰 Libraries Used

| Left Side Libraries        | Right Side Libraries       |
|----------------------------|----------------------------|
| `numpy`                    | `xgboost`                  |
| `pandas`                   | `lightgbm`                 |
| `matplotlib.pyplot`        | `catboost`                 |
| `seaborn`                  | `warnings`                 |
| `sklearn.model_selection`  | `sklearn.linear_model`     |
| `sklearn.preprocessing`    | `sklearn.ensemble`         |
| `sklearn.metrics`          |                            |



---

## 📊 Project Workflow

| Step                        | Description                                    |
|-----------------------------|------------------------------------------------|
| **Defining the Problem**     | Define the problem and project objectives.     |
| **Loading the Dataset**      | Import and load the Uber ride data.            |
| **Basic Cleaning**           | Clean the dataset by handling missing values.  |
| **Exploratory Data Analysis (EDA)** | Analyze and visualize the data.             |
| **Univariate and Bivariate Analysis** | Investigate individual and pairwise relationships between variables. |
| **Correlation Analysis**     | Analyze correlations between features.         |
| **Feature Engineering**      | Create new features or modify existing ones.   |
| **Preprocessing**            | Prepare data for modeling.                    |
| **Encoding Categorical Features** | Convert categorical data into numerical format. |
| **Scaling Numerical Features** | Normalize or standardize numerical features.   |
| **Model Building**           | Build various regression models.              |
| **Linear Regression**        | Apply linear regression.                      |
| **Random Forest**            | Implement random forest model.                |
| **XGBoost**                  | Implement XGBoost model.                      |
| **LightGBM**                 | Implement LightGBM model.                     |
| **CatBoost**                 | Implement CatBoost model.                     |
| **Model Evaluation**         | Evaluate models using RMSE and R² score.      |
| **Conclusion**               | CatBoost Regressor emerged as the best-performing model. |


---
## 📊 Load Dataset 

Sample: The dataset contains **300 rows** and **46 columns**. Below is a statistical summary of the columns:

| **Column**                 | **Count**   | **Mean**    | **Std**     | **Min**     | **25%**     | **50%**     | **75%**     | **Max**     |
|----------------------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| `timestamp`                | 300         | 1.541233e+09 | 3.293688e+06 | 1.540000e+09 | 1.540000e+09 | 1.540000e+09 | 1.540000e+09 | 1.550000e+09 |
| `hour`                     | 300         | 11.31       | 7.27        | 0           | 4           | 12          | 18          | 23          |
| `day`                      | 300         | 17.72       | 10.09       | 1           | 13          | 17          | 28          | 30          |
| `month`                    | 300         | 11.58       | 0.49        | 11          | 11          | 12          | 12          | 12          |
| `price`                    | 276         | 15.97       | 8.42        | 3           | 9.5         | 13.5        | 22.5        | 38.5        |
| `distance`                 | 300         | 2.20        | 0.97        | 0.44        | 1.17        | 2.44        | 3.05        | 4.43        |
| `surge_multiplier`         | 300         | 1.00        | 0.03        | 1           | 1           | 1           | 1           | 1.25        |
| `latitude`                 | 300         | 42.33       | 0.05        | 42.21       | 42.34       | 42.35       | 42.36       | 42.37       |
| `longitude`                | 300         | -71.07      | 0.02        | -71.11      | -71.08      | -71.06      | -71.05      | -71.03      |
| `temperature`              | 300         | 39.80       | 7.20        | 18.91       | 37.26       | 40.87       | 43.91       | 57.22       |
| **...**                    | **...**     | **...**     | **...**     | **...**     | **...**     | **...**     | **...**     | **...**     |

> **Note:** The dataset contains various features related to Uber ride data, including price, distance, surge multiplier, temperature, and more.

---

## Exploratory Data Analysis (EDA)

![EDA](https://github.com/user-attachments/assets/2f7abf08-bf65-416f-9c70-64b830b8f2da)

## ✅ Correlation matrix:

![Correlation](https://github.com/user-attachments/assets/1be729cf-9582-4b6e-841c-fcfb9b3050fa)

---

# Model Evaluation

## ✅ Predict and Evaluate

Below are the performance metrics (RMSE and R² Score) for each regression model used:

| Model              | RMSE     | R² Score |
|--------------------|----------|----------|
| Linear Regression  | 7.289921 | 0.264664 |
| Random Forest      | 2.833321 | 0.888921 |
| XGBoost            | 2.445294 | 0.917263 |
| LightGBM           | 2.527042 | 0.911638 |
| CatBoost           | 3.007453 | 0.874848 |

📌 **XGBoost** achieved the **lowest RMSE** and **highest R² score**, making it the best-performing model in this experiment.

✅ Visualize comparison:

![Da1](https://github.com/user-attachments/assets/da7da8f2-c248-43ca-9a47-f985336d33c9)

---

## 📈 Conclusion

From our model comparisons, **CatBoost Regressor** delivered the best performance based on evaluation metrics like **RMSE** and **R² Score**.  
It is recommended for future Uber price prediction tasks due to its robustness and superior accuracy.

---
