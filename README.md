# 🏡 Real Estate Sales Analysis – Linear Regression Model

## 👤 Author  
Ye Myat Oo  

---

## 📘 Overview  
The **Real Estate Sales Analysis Project** explores how machine learning—specifically **Linear Regression**—can be used to understand and predict property sale prices in Connecticut, USA.

Developed using **Python**, **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**, and **Scikit-Learn**, this project demonstrates skills in:

- Data preprocessing  
- Statistical analysis  
- Data visualisation  
- Machine learning model building  
- Cross-validation  
- Feature engineering  
- Clean and structured Jupyter Notebook development  

Originally created as an academic coursework project, this repository is refined for portfolio and professional presentation.

---

## 📂 Dataset  

**Source:** State of Connecticut – Data.gov  
**Dataset:** *Real Estate Sales 2001–2022 GL*  
**Original Size:** 1,097,629 rows  

### 📌 Note on Dataset Size  
The original dataset (**119 MB**) exceeds GitHub’s 100MB file-size limit and is therefore **not included** in the repository.  
A smaller **10,000-row sampled dataset (`real_estate_sampled.csv`)** is included for analysis, reproducibility, and testing.

Key columns include:

- List Year  
- Town  
- Address  
- Assessed Value  
- Sale Amount  
- Property Type  
- Sales Ratio  

During preprocessing:

- Columns with excessive missing data were removed  
- Categorical missing values were replaced with `"Unknown"`  
- Dataset was converted into a clean, analysis-ready form  

---

## 🔧 Project Workflow

### **1. Data Preparation**
- Removed unusable columns  
- Filled missing values  
- Sampled dataset to 10,000 entries  
- Ensured consistent formatting & structure  

---

### **2. Statistical Analysis**
Computed descriptive statistics using Pandas/NumPy:

- Mean, Median, Standard Deviation  
- Skewness & Kurtosis  
- Outlier identification  
- Distribution shape analysis  

Result: **Highly right-skewed** numerical columns due to extreme sale prices.

---

### **3. Visualisation**
Visualisations created using **Matplotlib** and **Seaborn**:

- Histogram of Sale Amount  
- Boxplot of Sale Amount  
- Histogram of Assessed Value  
- Correlation Matrix Heatmap  

📌 **Most important visualisation**  
The **Correlation Heatmap**, showing that *Assessed Value* has the strongest relationship with *Sale Amount*.

---

## 🤖 Machine Learning Model

### **Model:** Linear Regression (Scikit-Learn)

### **Features (X):**
- Assessed Value  
- Sales Ratio  
- List Year  

### **Target (y):**
- Sale Amount  

### **Model Results:**

| Metric | Value |
|--------|--------|
| **MSE** | ~3.02 × 10¹² |
| **R² Score** | 0.06 |

The low R² indicates non-linear behaviour and strong influence of outliers, making the dataset challenging for simple linear regression.

---

## 🧪 Validation  
Used **5-Fold Cross-Validation** to evaluate model stability:

- MSE varied significantly across folds  
- R² ranged from negative to moderately positive  
- Confirms non-linear complexity in the dataset  

---

## 🛠️ Feature Engineering  

Implemented the following enhancements:

- Polynomial Features (degree 2)  
- One-Hot Encoding for categorical columns  
- CountVectorizer for `Town` text data  
- Standard Scaling for numerical features  

---
