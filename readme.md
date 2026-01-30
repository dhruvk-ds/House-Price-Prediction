# 🏠 Housing Price Prediction -- Machine Learning

## 📌 Project Overview

This project predicts **median house prices** using the California
Housing dataset.\
It demonstrates a **complete end-to-end machine learning workflow**
including data splitting, feature engineering, preprocessing, model
training, evaluation, and model saving.

------------------------------------------------------------------------

## 🎯 Problem Statement

Given housing-related features such as location, population, rooms, and
income, predict the **median house value**.

This is a **regression problem**.

------------------------------------------------------------------------

## 🧠 ML Approach

### 🔹 Data Splitting

-   Used **StratifiedShuffleSplit**
-   Stratification based on **income category**
-   Ensures train and test sets have similar income distribution

### 🔹 Feature Engineering

-   Created `income_cat` using `pd.cut()` on `median_income`
-   Removed `income_cat` after splitting to avoid data leakage

------------------------------------------------------------------------

## 🔧 Preprocessing

### Numeric Features

-   Missing values handled using **SimpleImputer (median)**
-   Features scaled using **StandardScaler**

### Categorical Features

-   Encoded using **OneHotEncoder**

### Tool Used

-   **ColumnTransformer** for clean preprocessing

------------------------------------------------------------------------

## 🤖 Models Used

-   Linear Regression
-   Decision Tree Regressor
-   Random Forest Regressor

------------------------------------------------------------------------

## 📈 Model Evaluation

-   Evaluated using **Root Mean Squared Error (RMSE)**
-   Cross-validation used for reliable performance estimation

------------------------------------------------------------------------

## 🏗️ Production Logic

-   Model is trained only if it does not already exist:

``` python
if not os.path.exists("model.pkl"):
    # train and save model
```

-   Prevents unnecessary retraining

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   Python
-   Pandas
-   NumPy
-   Scikit-learn
-   Joblib
-   Matplotlib

------------------------------------------------------------------------

## 📂 Project Structure

    housing-ml/
    │
    ├── housing.csv
    ├── input.csv
    ├── main.py
    ├── model.pkl
    ├── requirements.txt
    ├── README.md

------------------------------------------------------------------------

## ⚙️ How to Run the Project

``` bash
pip install -r requirements.txt
python main.py
```

------------------------------------------------------------------------

## 📌 Key Learnings

-   Stratified sampling
-   Feature engineering for regression
-   End-to-end ML pipelines
-   Model persistence
-   Regression model evaluation

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Hyperparameter tuning
-   Feature selection
-   Advanced regression models
-   Model deployment

------------------------------------------------------------------------

## 👤 Author

Dhruv Kashyap\
Aspiring Data Scientist \| Python \| Machine Learning
