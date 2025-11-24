🏡 Real Estate Sales Analysis – Linear Regression Model
👤 Author

Ye Myat Oo

📘 Overview

The Real Estate Sales Analysis Project explores how machine learning—specifically Linear Regression—can be used to understand and predict property sale prices in Connecticut, USA.

This project was developed using Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-Learn.
It focuses on data preprocessing, statistical analysis, visualisation, model development, and feature engineering.

This repository demonstrates practical experience in:

Data cleaning & preprocessing

Exploratory data analysis

Statistical distribution analysis

Data visualisation with graphs

Machine Learning (Linear Regression)

Cross-validation & model evaluation

Feature engineering & scaling

Originally developed as an academic coursework project, this version is polished for portfolio and professional use.

📂 Dataset

Source: State of Connecticut – Data.gov
Dataset: Real Estate Sales 2001–2022 GL
Original Size: 1,097,629 rows
Sampled Size: 10,000 rows (for faster, smoother processing)

Key columns include:

List Year

Town

Address

Assessed Value

Sale Amount

Property Type

Sales Ratio

During preprocessing:

Columns with extreme missing data were removed

Categorical columns were filled with "Unknown"

Dataset was transformed into a clean 1NF-ready format

🔧 Project Workflow
1. Data Preparation

Removed noisy/unusable columns

Filled missing categorical entries

Sampled dataset to 10,000 records

Ensured consistent formatting & types

2. Statistical Analysis

Computed key descriptive statistics:

Mean, median, standard deviation

Skewness & kurtosis

Identification of outliers & distribution shape

Result: Highly right-skewed distributions due to extreme property prices.

3. Visualisation

Created visual insights using Matplotlib & Seaborn:

Histogram of Sale Amount

Boxplot of Sale Amount

Histogram of Assessed Value

Correlation Matrix Heatmap

📌 Most important plot:
The Correlation Heatmap, which confirms that Assessed Value is the strongest predictor of Sale Amount.

🤖 Machine Learning Model
Model Used: Linear Regression
Features:

Assessed Value

Sales Ratio

List Year

Target:

Sale Amount

Results:
Metric	Value
MSE	~3.02 × 10¹²
R²	0.06

The model shows that while some linear correlation exists, the dataset contains strong non-linear patterns and many outliers.

🧪 Validation

Used 5-Fold Cross Validation to evaluate consistency:

MSE values varied across folds

R² values ranged from negative to moderately positive

Confirms model instability due to dataset complexity

🛠️ Feature Engineering

To improve predictive power, the following were implemented:

Polynomial Features (degree 2)

One-Hot Encoding for categorical variables

CountVectorizer for textual “Town” data

StandardScaler for numerical feature scaling
