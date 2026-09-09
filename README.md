#  Car Price Prediction Using Machine Learning

A machine learning regression project that predicts the **selling price of used cars** based on various factors such as car age, present price, mileage, fuel type, transmission, seller type, owner history, and brand.

This project was developed as a **self-driven Machine Learning project** to strengthen my practical understanding of data preprocessing, exploratory data analysis, feature engineering, categorical encoding, regression modeling, and model evaluation.

---

##  Project Overview

The used-car market contains several factors that influence the resale value of a vehicle. The objective of this project is to build a machine learning model that can learn from historical car data and predict the expected selling price of a used car.

The project follows a complete machine learning workflow:

**Data Collection → Data Cleaning → Feature Engineering → EDA → Encoding → Model Training → Evaluation → Feature Importance**

---

##  Objectives

* Analyze factors affecting used-car prices
* Clean and preprocess the dataset
* Handle missing and duplicate values
* Standardize inconsistent categorical values
* Calculate **Car Age** from the manufacturing year
* Extract **Brand** from the car name
* Perform exploratory data analysis
* Encode categorical variables using One-Hot Encoding
* Train multiple regression models
* Compare model performance using MAE, RMSE, and R²
* Identify the most important features influencing car prices

---

##  Technologies Used

* **Python**
* **Pandas** – Data manipulation and preprocessing
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine Learning
* **Jupyter Notebook** – Development environment

---

##  Dataset

The dataset contains information about used cars, including:

| Feature         | Description                     |
| --------------- | ------------------------------- |
| `Car_Name`      | Name of the car                 |
| `Year`          | Manufacturing year              |
| `Selling_Price` | Target variable – selling price |
| `Present_Price` | Current/ex-showroom price       |
| `Kms_Driven`    | Kilometers driven               |
| `Fuel_Type`     | Fuel type of the car            |
| `Seller_Type`   | Individual or dealer            |
| `Transmission`  | Manual or automatic             |
| `Owner`         | Number of previous owners       |

---

##  Data Preprocessing

The following preprocessing steps were performed:

* Checked dataset shape and data types
* Identified missing values
* Handled null values where required
* Checked and removed duplicate records
* Standardized categorical values
* Checked unique values in categorical columns
* Removed unnecessary columns

---

##  Feature Engineering

### 1. Car Age

A new feature called `Car_Age` was created using:

```text
Car Age = Current Year - Manufacturing Year
```

This helps the model understand how the age of a vehicle affects its resale value.

### 2. Brand Extraction

The car brand was extracted from the `Car_Name` column.

For example:

```text
"Maruti Swift Dzire VDI" → "Maruti"
"Hyundai i20" → "Hyundai"
"Honda City" → "Honda"
```

---

##  Exploratory Data Analysis

Several visualizations were created to understand the dataset and identify important patterns.

### Selling Price Distribution

The distribution of selling prices was analyzed to understand the overall price range and identify potential skewness or outliers.

### Selling Price vs Fuel Type

A box plot was used to compare selling prices across different fuel types.

### Selling Price vs Car Age

A scatter plot was used to investigate the relationship between vehicle age and selling price.

### Correlation Heatmap

A correlation heatmap was created to understand relationships between numerical features and identify variables that may have a strong relationship with selling price.

---

##  Categorical Encoding

Categorical features were converted into numerical form using **One-Hot Encoding**.

Example:

```python
X = pd.get_dummies(X, drop_first=True)
```

This allows machine learning algorithms to work with categorical variables.

---

##  Machine Learning Models

Two regression algorithms were trained and compared:

### 1. Linear Regression

Linear Regression was used as a baseline regression model to understand the relationship between input features and selling price.

### 2. Random Forest Regressor

Random Forest Regressor was used to capture non-linear relationships between car characteristics and selling price.

---

##  Model Evaluation

The models were evaluated using three important regression metrics:

### MAE – Mean Absolute Error

Measures the average absolute difference between actual and predicted prices.

**Lower MAE = Better performance**

### RMSE – Root Mean Squared Error

Measures prediction error while giving more weight to larger errors.

**Lower RMSE = Better performance**

### R² Score

Measures how well the model explains the variation in the target variable.

**Higher R² = Better performance**

Model Comparison
Model	             MAE	      RMSE	      R² Score
Random Forest	     72,912.17	127,158.23	0.926276
Gradient Boosting	 81,660.42	127,735.84	0.925605
Linear Regression  133,098.53	261,925.34	0.687195

> **Note:** The final values will be updated after model training and evaluation.

---

##  Feature Importance

Feature importance was analyzed using the best-performing model to identify which factors contribute most to used-car price prediction.

The analysis helps answer questions such as:

* Does present price strongly influence resale price?
* How much does car age affect the selling price?
* Does mileage impact the predicted price?
* How important are fuel type and transmission?

---

##  Key Insights

Some important observations from the analysis include:

* Vehicle age can have a significant impact on resale value.
* Cars with higher present prices generally tend to have higher selling prices.
* Mileage can influence the resale value of a used car.
* Fuel type and transmission can contribute to differences in selling prices.
* Tree-based models such as Random Forest can capture non-linear relationships that may not be captured effectively by a simple Linear Regression model.

---

##  Project Explanation Video

I also created a **project explanation video** where I explain the complete workflow of this Car Price Prediction project, including:

* Problem statement
* Dataset and features
* Data preprocessing
* Feature engineering
* Exploratory Data Analysis
* Machine learning models
* Model evaluation
* Feature importance
* Final outcome

The video has been shared on **GitHub and LinkedIn** as part of my project portfolio.


 **LinkedIn Video:** -- https://lnkd.in/p/dbeD8gF5
 

>  The video demonstrates my understanding of the project and explains how the machine learning pipeline was implemented.

---

##  Project Structure

```text
Car-Price-Prediction/
│
├── Car_Price_Prediction.ipynb
├── car_data.csv
├── README.md
│
└── images/
    ├── price_distribution.png
    ├── price_vs_fuel.png
    ├── price_vs_age.png
    ├── correlation_heatmap.png
    └── feature_importance.png
```

---

##  How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/Car-Price-Prediction.git
```

### 2. Navigate to the project directory

```bash
cd Car-Price-Prediction
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
Car_Price_Prediction.ipynb
```

Run the notebook cells sequentially.

---

##  Future Improvements

This project can be further improved by:

* Testing Gradient Boosting and XGBoost models
* Hyperparameter tuning
* Cross-validation
* Handling outliers more extensively
* Building a simple web application using Flask or Streamlit
* Adding a user interface for real-time car price prediction
* Deploying the trained model as a prediction service

---

##  Author

**Prajna Mondal**

B.Tech – Computer Science & Engineering

Interested in **Data Analytics, Machine Learning, Python, SQL, and Data Visualization**.

---

##  Project Highlights

**✔ End-to-end Machine Learning workflow**

**✔ Data Cleaning & Preprocessing**

**✔ Feature Engineering**

**✔ Exploratory Data Analysis**

**✔ Categorical Encoding**

**✔ Regression Modeling**

**✔ Model Comparison**

**✔ MAE, RMSE & R² Evaluation**

**✔ Feature Importance Analysis**

**✔ Project Explanation Video**

---

##  License

This project is created for **learning, portfolio development, and educational purposes**.

Thank you.
