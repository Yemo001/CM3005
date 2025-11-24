# CM3005

📊 Real Estate Sales Analysis – Linear Regression Model

A CM3005 Data Science Coursework Project

📌 Overview

This project applies data preprocessing, statistical analysis, data visualisation, and a linear regression model to understand factors influencing property prices in Connecticut (USA).
The objective is to demonstrate how machine learning can model real-world pricing patterns using structured numerical and categorical features.

This repository contains:

The full Jupyter Notebook (.ipynb)

The PDF export of the report

Cleaned dataset used for the project

Supporting scripts and outputs

📂 Dataset

Source: Real Estate Sales 2001–2022 (State of Connecticut, Data.gov)
Original Size: 1,097,629 rows, 14 columns
Processed Size: 10,000 sampled rows (to improve performance on local machines)

The dataset includes fields such as:

Serial Number

List Year

Town

Address

Assessed Value

Sale Amount

Property Type

Sales Ratio

Residential Type

During preprocessing:

Columns with excessive missing values (e.g., OPM remarks, Assessor Remarks, Non Use Code) were removed.

Missing categorical values were filled with "Unknown".

Dataset was transformed into a clean 1NF structure.

🔧 Project Workflow
1. Data Preprocessing

Handle missing values

Drop unsuitable columns

Sample the dataset for computational efficiency

Convert the dataset into a cleaned format for analysis

2. Statistical Analysis

Performed using pandas and NumPy, including:

Mean, Median, Standard Deviation

Skewness + Kurtosis (to identify outliers & distribution shape)

Key finding:
The dataset contains strong right-skewed distributions due to extreme property prices.

📈 Visualisations

Using Matplotlib and Seaborn, the notebook includes:

Histogram of Sale Amount

Boxplot of Sale Amount (outlier detection)

Histogram of Assessed Value

Correlation heatmap for numeric variables

Most important visualisation:

🔥 Correlation Matrix

Reveals that Assessed Value has the strongest positive correlation with Sale Amount, making it a key predictive feature.

🤖 Machine Learning Model
Model Used: Linear Regression (Scikit-Learn)
Features (X):

Assessed Value

Sales Ratio

List Year

Target (y):

Sale Amount

Results:

Metric	Value
MSE	~3.02 × 10¹²
R²	~0.06

Cross-validation (k=5) was also performed to validate model stability.

🧪 Validation

5-Fold Cross Validation

R² scores varied across folds, confirming the presence of non-linear effects and outliers

Reinforces the potential benefit of feature engineering or transforming variables

🛠️ Feature Engineering

To improve model performance, the following were implemented:

Polynomial Features (degree 2)

One-Hot Encoding for categorical features

CountVectorizer for text-based town data

Standard Scaling for numerical variables
