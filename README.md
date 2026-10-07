# 🏦 Bank GoodCredit – Credit Risk Prediction

## 📌 Project Overview

This project develops a Machine Learning system to predict whether a customer is likely to have a good or bad credit history.

The target variable is `Bad_label`:

- `0` → Good credit history
- `1` → Bad credit history / 30+ days past due

The project uses three datasets containing customer demographic information, credit-account information, and credit-enquiry information. These datasets are transformed into customer-level features and used to develop and evaluate classification models for credit-risk prediction.

## 🎯 Business Objective

The main objective is to help Bank GoodCredit identify customers who are more likely to have poor credit behaviour.

A reliable credit-risk model can help:

- Assess customer creditworthiness
- Identify high-risk customers
- Reduce potential credit-default risk
- Improve lending and credit decisions
- Support risk-based customer management

## 📂 Datasets

The project uses three datasets:

### 1. Cust_Account

Contains customer credit-account and repayment information, including:

- Account type
- Account ownership
- Account opening and closing dates
- Current balance
- High credit amount
- Credit limit
- Cash limit
- Past-due amount
- Payment information
- Interest rate
- Payment frequency
- Actual payment amount

### 2. Cust_Enquiry

Contains historical credit-enquiry information, including:

- Customer number
- Enquiry date
- Enquiry purpose
- Enquiry amount
- Upload date

### 3. Cust_Demographics

Contains customer demographic/application information and the target variable `Bad_label`.

## 📌 Dataset Availability

The project was developed using three datasets:

- `Cust_Account.csv`
- `Cust_Enquiry.csv`
- `Cust_Demographics.csv`

Due to the large size of `Cust_Account.csv` and data-distribution considerations, the complete Account dataset is not included in this public GitHub repository.

The `Cust_Enquiry.csv` and `Cust_Demographics.csv` files are included in the `Bank_GoodCredit_Data` folder.

The notebook contains the complete data-processing and feature-engineering workflow used with the original Account dataset.

## 📊 Dataset Size

| Dataset | Rows | Columns |
|---|---:|---:|
| Cust_Account | 186,329 | 21 |
| Cust_Enquiry | 413,188 | 6 |
| Cust_Demographics | 23,896 | 83 |

After customer-level feature engineering and data preparation:

- Training records: 19,116
- Testing records: 4,780
- Numerical features: 104
- Categorical features: 44

The target distribution was approximately:

- Good Credit (`0`): 95.8%
- Bad Credit (`1`): 4.2%

This indicates a significant class imbalance.

## 🔄 Project Workflow

```text
Data Collection
       ↓
Data Understanding
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Account Feature Engineering
       ↓
Enquiry Feature Engineering
       ↓
Demographic Data Preparation
       ↓
Customer-Level Data Integration
       ↓
Feature Selection
       ↓
Train-Test Split
       ↓
Data Preprocessing
       ↓
Baseline Models
       ↓
Hyperparameter Tuning
       ↓
Cross-Validation
       ↓
Model Comparison
       ↓
ROC-AUC & Gini Evaluation
       ↓
Feature Importance
       ↓
Rank Ordering / Decile Analysis
       ↓
Final Model
       ↓
Credit Risk Prediction

