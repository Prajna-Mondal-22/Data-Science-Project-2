#  Car Price Prediction with Machine Learning

A Machine Learning regression project that predicts the **selling price of used cars** based on features such as car age, mileage, fuel type, seller type, transmission, owner history, engine capacity, maximum power, seats, and brand.

This project was completed as part of **Oasis Infobyte — Task 3**.

---

##  Project Overview

The objective of this project is to build and compare multiple Machine Learning regression models for predicting used-car selling prices.

The project covers the complete Machine Learning workflow:

* Data loading and inspection
* Data cleaning and preprocessing
* Missing-value handling
* Duplicate removal
* Feature engineering
* Exploratory Data Analysis (EDA)
* Categorical feature encoding
* Train-test splitting
* Regression model training
* Model evaluation and comparison

---

##  Objective

Build a regression model capable of predicting the **selling price of a used car** using relevant vehicle characteristics.

**Target Variable:** `selling_price`

---

## 📊 Dataset

The project uses a used-car dataset containing **8,128 records and 12 original features**.

### Original Features

| Feature              | Description                |
| -------------------- | -------------------------- |
| `name`               | Name of the car            |
| `year`               | Manufacturing year         |
| `selling_price`      | Selling price of the car   |
| `km_driven`          | Kilometers driven          |
| `fuel`               | Fuel type                  |
| `seller_type`        | Type of seller             |
| `transmission`       | Transmission type          |
| `owner`              | Previous owner information |
| `mileage(km/ltr/kg)` | Mileage                    |
| `engine`             | Engine capacity            |
| `max_power`          | Maximum power              |
| `seats`              | Number of seats            |

---

##  Technologies Used

* **Python**
* **Pandas** — Data manipulation
* **NumPy** — Numerical computation
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Scikit-learn** — Machine Learning and preprocessing
* **Jupyter Notebook / Google Colab**

---

##  Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Inspected dataset dimensions and data types.
3. Checked missing values.
4. Checked and removed duplicate records.
5. Cleaned categorical variables using string formatting.
6. Converted `max_power` into a numerical data type.
7. Handled missing numerical values using **median imputation**.
8. Created a new feature:

   * `car_age = 2026 - year`
9. Extracted the car **brand** from the `name` column.
10. Removed unnecessary columns such as `name` and `year`.
11. Applied **One-Hot Encoding** to categorical variables.
12. Split the dataset into training and testing sets.

### Train-Test Split

* **80% Training Data**
* **20% Testing Data**
* `random_state = 42`

---

##  Exploratory Data Analysis

The project includes visual analysis of:

### 1. Selling Price Distribution

A histogram was used to understand the distribution of car selling prices.

### 2. Selling Price vs Car Age

A scatter plot was used to analyze the relationship between vehicle age and selling price.

### 3. Top Car Brands

The top 15 brands by number of listings were visualized using a bar chart.

---

##  Machine Learning Models

Three regression algorithms were trained and evaluated:

### 1. Linear Regression

A baseline regression model used to understand the linear relationship between vehicle features and selling price.

### 2. Random Forest Regressor

An ensemble learning algorithm that combines multiple decision trees to improve prediction performance.

Parameters used:

* `n_estimators = 200`
* `random_state = 42`
* `n_jobs = -1`

### 3. Gradient Boosting Regressor

An ensemble boosting algorithm that builds models sequentially to improve prediction accuracy.

Parameters used:

* `n_estimators = 200`
* `learning_rate = 0.05`
* `max_depth = 3`
* `random_state = 42`

---

##  Model Performance

The models were evaluated using:

* **MAE — Mean Absolute Error**
* **RMSE — Root Mean Squared Error**
* **R² Score — Coefficient of Determination**

| Model             |           MAE |           RMSE |   R² Score |
| ----------------- | ------------: | -------------: | ---------: |
| Linear Regression |    133,098.53 |     261,925.34 |     0.6872 |
| Random Forest     | **72,912.17** | **127,158.23** | **0.9263** |
| Gradient Boosting |     81,660.42 |     127,735.84 |     0.9256 |

###  Best Performing Model

**Random Forest Regressor** achieved the best overall performance:

* **MAE:** 72,912.17
* **RMSE:** 127,158.23
* **R² Score:** 0.9263

An R² score of **0.9263** indicates that the model explains approximately **92.63% of the variance** in the test-set selling prices.

---

##  Key Findings

* Random Forest performed significantly better than Linear Regression.
* Gradient Boosting also achieved strong predictive performance.
* Vehicle-related characteristics provide useful information for estimating used-car prices.
* The ensemble tree-based models were better suited to this dataset than the simple linear model.
* Random Forest produced the highest R² score among the three tested models.

---

##  Project Structure

```text
Car-Price-Prediction/
│
├── OASIS_task_3.ipynb
├── cardekho_task_3.csv
└── README.md
```

---

##  How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Car-Price-Prediction.git
```

### 2. Navigate to the project directory

```bash
cd Car-Price-Prediction
```

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 4. Open the notebook

```bash
jupyter notebook OASIS_task_3.ipynb
```

Alternatively, upload the notebook to **Google Colab**.

### 5. Run all cells

Make sure `cardekho_task_3.csv` is available in the working directory or upload it when prompted.

---

##  Future Improvements

The project can be further improved by:

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Trying XGBoost or other advanced boosting algorithms
* Performing feature importance analysis
* Applying cross-validation
* Handling potential outliers
* Creating an interactive car price prediction application
* Deploying the final model using Flask or Streamlit

---

##  Author

**Prajna Mondal**

B.Tech — Computer Science & Engineering

### Technical Skills

`Python` · `SQL` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `Seaborn` · `Power BI` · `Excel`

---

##  Internship

**Oasis Infobyte — Python Developer Internship**

**Task 3:** Car Price Prediction with Machine Learning

---

 If you found this project useful, consider giving the repository a star! Thank You .
