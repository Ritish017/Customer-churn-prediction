# Customer Churn Prediction

This repository contains the implementation of **Task 3: Customer Churn Prediction** as part of the provided requirements. The project predicts whether a customer will discontinue a subscription-based service using historical data and provides insights into the key factors driving churn.

## Task Objectives

The goal of this project is to:

- Build a machine learning model to predict customer churn (whether a customer will leave a subscription service).
- Analyze historical customer data, including usage patterns (e.g., number of products, activity status), demographic details (e.g., age, gender, geography), and subscription duration (e.g., tenure).
- Handle potential missing values with appropriate imputation strategies (though none were found in the dataset).
- Deliver a model that effectively identifies customers likely to churn and highlights the most significant factors contributing to churn.

## Dataset

The project uses the `Churn_Modelling.csv` dataset, which includes features like:

- `CreditScore`
- `Geography`
- `Gender`
- `Age`
- `Tenure`
- `Balance`
- `NumOfProducts`
- `HasCrCard`
- `IsActiveMember`
- `EstimatedSalary`
- Target variable: `Exited` (1 = churned, 0 = stayed)

## Steps to Run the Project

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/your-username/customer-churn-prediction.git
   cd customer-churn-prediction
2.**Install Dependencies**:
Install the required Python libraries using:
bash

pip install pandas numpy scikit-learn xgboost matplotlib seaborn

3.**Prepare the Dataset**:
Ensure Churn_Modelling.csv is in the repository root or update the file path in the notebook (churn_prediction.ipynb) to match your local setup.

If not included, download it from Kaggle and place it in the root directory.

4.**Run the Notebook**:
Launch Jupyter Notebook and open the project:
bash

jupyter notebook churn_prediction.ipynb

Execute all cells to preprocess the data, train models, and view results.

## Expected Output
->A trained XGBoost model with ROC-AUC > 0.80.

->Visualizations (e.g., feature importance, confusion matrix, ROC curve).

->Insights into key churn drivers (e.g., Age, Balance, NumOfProducts).

## Project Structure
churn_prediction.ipynb: The main notebook containing the full pipeline (EDA, feature engineering, modeling, evaluation).

Churn_Modelling.csv: The dataset used for analysis (optional; may need to be downloaded separately).

README.md: This documentation file.

## Implementation Details
**Data Preprocessing**:
Dropped irrelevant columns (e.g., RowNumber, CustomerId) that don’t contribute to prediction.

Encoded categorical variables (e.g., Gender as binary, Geography with one-hot encoding).

Scaled numerical features using StandardScaler for consistent model input.

**Feature Engineering*:
 Added features like HasZeroBalance (1 if balance is zero), BalanceToSalaryRatio (balance/salary), and LoyalityScore (products * balance * tenure) to enhance predictive power.

**Modeling**:
 Trained Random Forest and XGBoost classifiers.

Performed hyperparameter tuning using GridSearchCV to optimize model performance.

**Evaluation**:
 Used classification reports, ROC-AUC scores, confusion matrices, and feature importance plots to assess performance and identify churn factors.

**Results**
 Best Model: Tuned XGBoost with ROC-AUC ~0.85 (varies slightly with tuning).

 Key Churn Factors: Age, Balance, NumOfProducts, and IsActiveMember emerged as top contributors based on feature importance.

