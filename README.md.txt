# Bank Customer Churn Prediction

This project aims to predict customer churn using the [Churn_Modelling](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-fraud) dataset. By employing feature engineering, exploratory data analysis (EDA), and machine learning models (Random Forest and XGBoost), we strive to achieve accurate predictions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Technologies Used](#technologies-used)
3. [Dataset](#dataset)
4. [Getting Started](#getting-started)
5. [Project Structure](#project-structure)
6. [Key Steps in the Analysis](#key-steps-in-the-analysis)
7. [Model Evaluation](#model-evaluation)
8. [Contributing](#contributing)
9. [License](#license)

## Project Overview
The objective of this project is to identify customers who are likely to churn from a bank. The project uses historical customer data to build predictive models that can aid in retention strategies.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

## Dataset
The dataset used for this analysis is the `Churn_Modelling.csv` file, which contains data about bank customers, including demographics, account information, and churn status.

### Features:
- `CreditScore`: Credit score of the customer.
- `Gender`: Gender of the customer.
- `Age`: Age of the customer.
- `Tenure`: Number of years the customer has been with the bank.
- `Balance`: Account balance.
- `NumOfProducts`: Number of products the customer has with the bank.
- `HasCrCard`: Whether the customer has a credit card.
- `IsActiveMember`: Whether the customer is an active member.
- `EstimatedSalary`: Estimated salary of the customer.
- `Exited`: Target variable indicating if the customer has churned (1) or not (0).

## Getting Started
To run this project locally, clone the repository and follow the instructions below.

```bash
# Clone the repository
git clone https://github.com/yourusername/bank-customer-churn-prediction.git

# Navigate to the project directory
cd bank-customer-churn-prediction

# Install required packages
pip install -r requirements.txt

# Run the Jupyter Notebook
jupyter notebook
