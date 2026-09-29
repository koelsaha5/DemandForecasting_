#  Demand Forecasting using XGBoost

##  Project Overview

This project focuses on **predicting product demand** using machine learning. The objective is to analyze different factors such as price, discount, inventory, promotion, competitor pricing, and product category to predict the expected demand for a product.

The project follows an end-to-end machine learning workflow, starting from **data exploration and preprocessing** to **model training, hyperparameter tuning, evaluation, and model saving**.

---
link to website : (http://localhost:8501/)
##  Objective

The main objective of this project is to build a machine learning model that can accurately predict **Demand**, which is a continuous numerical value.

This can help businesses understand demand patterns and support better planning and decision-making.

---

##  Dataset

- **Rows:** 76,000
- **Columns:** 16
- **Total data points:** Approximately 1.216 million
- **Target variable:** `Demand`

The dataset contains information related to products, pricing, inventory, promotions, competitor pricing, and product categories.

---

##  Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to:

- Understand the structure of the dataset
- Check the distribution of variables
- Identify patterns and relationships
- Analyze the relationship between features and demand
- Identify relevant features for machine learning

---

##  Data Preprocessing

The following preprocessing steps were performed:

1. Selected the relevant features for prediction.
2. Handled categorical data using **Label Encoding**.
3. Separated the independent variables (`X`) and target variable (`y`).
4. Split the dataset into:
   - **80% Training Data**
   - **20% Testing Data**

---

## 🤖 Machine Learning Model

### XGBoost Regressor

The project uses **XGBoost (Extreme Gradient Boosting)** for demand prediction.

XGBoost is an ensemble learning algorithm based on decision trees. It builds trees sequentially, where each new tree attempts to reduce the errors made by the previous trees.

### Why XGBoost?

- Works well with structured/tabular data
- Can capture non-linear relationships
- Provides strong predictive performance
- Supports feature importance analysis
- Suitable for regression problems

---

##  Hyperparameter Tuning

To improve the model's performance, **RandomizedSearchCV** was used.

RandomizedSearchCV randomly tests different combinations of hyperparameters and evaluates them using **cross-validation**.

In this project:

- **25 parameter combinations** were tested.
- **3-fold cross-validation** was used.

This helped identify a better combination of XGBoost hyperparameters.

---

##  Model Evaluation

The model was evaluated using **RMSE (Root Mean Squared Error)**.

### RMSE

RMSE measures how far the predicted values are from the actual values.

- Lower RMSE → predictions are closer to actual values
- Higher RMSE → larger prediction errors

RMSE was selected because this is a **regression problem** where the target variable, Demand, is continuous.

---

##  Feature Importance

Feature importance was analyzed to understand which input variables contributed most to the model's predictions.

This helps provide insight into which factors have a greater influence on product demand.

---

##  Model Saving

After training and tuning, the trained XGBoost model was saved using **Pickle**.

This allows the trained model to be reused later without retraining it from scratch.

---

##  Project Workflow

```text
Raw Dataset
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Selection
     ↓
Label Encoding
     ↓
Train-Test Split
     ↓
XGBoost Regressor
     ↓
RandomizedSearchCV
     ↓
Hyperparameter Tuning
     ↓
Model Prediction
     ↓
RMSE Evaluation
     ↓
Feature Importance
     ↓
Save Model using Pickle
```

---

##  Technologies Used

- **Python**
- **Pandas** – Data manipulation
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Data visualization
- **Scikit-learn** – Preprocessing, model selection and evaluation
- **XGBoost** – Machine learning model
- **Pickle** – Model serialization
- **Jupyter Notebook / Google Colab** – Development environment

---

##  Project Structure

```text
Demand-Forecasting/
│
├── data/
│   └── demand_forecasting.csv
│
├── notebooks/
│   ├── analysis.ipynb
│   └── machine_learning.ipynb
│
├── model/
│   └── xgboost_model.pkl
│
├── README.md
└── requirements.txt
```

> The exact folder/file names can be adjusted to match your GitHub repository.

---

##  How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### 3. Open the notebook

Run the notebooks in Jupyter Notebook or Google Colab.

### 4. Run the workflow

Execute the cells sequentially to:

- Load the dataset
- Perform EDA
- Preprocess the data
- Train the XGBoost model
- Perform hyperparameter tuning
- Evaluate the model
- Analyze feature importance
- Save the trained model

---

## 💡 Key Challenges

Some of the main challenges faced during the project were:

- Identifying the most relevant features for demand prediction
- Converting categorical data into a format suitable for machine learning
- Selecting appropriate XGBoost hyperparameters
- Improving model performance through hyperparameter tuning
- Evaluating the model using an appropriate regression metric

---

##  Key Learning

Through this project, I gained practical experience in:

- Exploratory Data Analysis
- Data preprocessing
- Feature selection
- Regression modelling
- XGBoost
- Hyperparameter tuning
- Cross-validation
- RMSE-based model evaluation
- Feature importance analysis
- Saving and reusing machine learning models

---

##  Author

**Koel Saha**

Machine Learning | Data Analytics | Python | SQL
