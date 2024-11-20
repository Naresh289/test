# 🏠 Mortgage Default Risk Prediction Model

## 📖 Overview
This project focuses on building a predictive model for **mortgage default risk** using a synthetic dataset. The model leverages various data science techniques, including **feature engineering**, **feature selection**, and **advanced machine learning algorithms**, to assess the likelihood of a borrower defaulting on their mortgage. 📊

---

## 📂 Dataset
The dataset used in this project is a **Synthetic Mortgage Performance Dataset**, containing the following key features:

- **Loan ID**: Unique identifier for each loan.
- **Borrower Age**: Age of the borrower.
- **Income Level**: Annual income of the borrower.
- **Credit Score**: Credit score of the borrower.
- **Loan Amount**: Total loan amount.
- **Property Value**: Value of the property being mortgaged.
- **Loan-to-Value Ratio**: Ratio of the loan amount to the property value.
- **Employment Status**: Borrower's employment status.
- **Payment History**: History of loan payments.
- **Economic Indicators**: Various macroeconomic factors like GDP growth, unemployment rate, etc.
- **Default Status**: Target variable indicating whether the borrower defaulted (`1`) or not (`0`).

---

## 🔧 Steps in the Model Development

### 1️⃣ Data Preprocessing
- **Handling Missing Values**: Filled missing economic indicator values using the forward fill (`ffill`) method.
- **Feature Scaling**: Applied scaling to all numerical features to ensure fair contribution to the model.
- **Encoding Categorical Variables**: Encoded categorical variables appropriately.
- **Exploratory Data Analysis (EDA)**: Conducted to understand data distributions, correlations, and potential outliers.

---

### 2️⃣ Feature Engineering
- **Debt-to-Income (DTI) Ratio**: Calculated to assess the borrower's debt relative to income.
- **Credit Utilization**: Removed due to redundancy.
- **Economic Stress Indicator**: Derived using Principal Component Analysis (PCA) on macroeconomic factors like GDP growth, unemployment rate, interest rate, and inflation rate.
- **Credit History Relative to Loan Issue Date**: Evaluated the relevance of the borrower’s credit history to the loan.

---

### 3️⃣ Feature Selection
Implemented a custom function `remove_highly_correlated_features` to remove features with a correlation greater than `0.8`, ensuring that only the most impactful and independent features were retained.

---

### 4️⃣ Model Development
Built and tested the following machine learning models to predict mortgage default risk:

- **Logistic Regression**
- **Random Forest Classifier**
- **XGBoost Classifier**
- *(Optional Advanced)* **Neural Network**

---

### 5️⃣ Model Evaluation
The models were evaluated using the following metrics:

- **Precision**: Proportion of true positives among all positive predictions.
- **Recall**: Proportion of true positives among actual positives.
- **ROC-AUC Curve**: Measures the model’s ability to distinguish between default and non-default cases.
- **Confusion Matrix**: Visualizes true vs. predicted classifications.
- **Feature Importance**: Identified the most influential features in the prediction.

---

### 6️⃣ Advanced Features
- **Cross-Validation**: Applied to ensure the models' robustness.
- **Model Interpretability Report**: Provided insights into how models make predictions.
- **Risk Scoring Mechanism**: Developed a system for quantifying default risk.
- **Business Recommendations**: Suggested actionable insights to improve decision-making.

---

## ⚙️ Requirements
Make sure the following libraries are installed in your Python environment:

- Python 3.x
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- NumPy

---

## ▶️ How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/mortgage-default-risk.git
2. Install the required libraries:
   - pip install -r requirements.txt
3. Run the Jupyter notebooks in sequence:
   - credit_risk_data_creation.ipynb to create the required dataset.
   - credit_risk_data_EDA.ipynb to explore the dataset.
   - credit_risk_modeling.ipynb to execute feature engineering, selection, model training and analyze the results.

📈 Conclusion
This project demonstrates the process of building a mortgage default risk prediction model, from data creation, data preprocessing and feature engineering to model development and evaluation. The final model helps assess the likelihood of mortgage defaults and provides valuable insights for financial decision-making. 💡

💡 Business Use Cases
Risk Assessment: Assist financial institutions in identifying high-risk borrowers.
Portfolio Optimization: Help optimize loan portfolios by minimizing potential defaults.
Policy Adjustments: Enable the creation of borrower-friendly policies to reduce defaults.
