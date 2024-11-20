Mortgage Default Risk Prediction Model
Overview
This project focuses on building a predictive model for mortgage default risk using a synthetic dataset. The model leverages various data science techniques, including feature engineering, feature selection, and advanced machine learning algorithms, to assess the likelihood of a borrower defaulting on their mortgage.

Dataset
The dataset used in this project is a Synthetic Mortgage Performance Dataset, containing the following key features:

Loan ID: Unique identifier for each loan.
Borrower Age: Age of the borrower.
Income Level: Annual income of the borrower.
Credit Score: Credit score of the borrower.
Loan Amount: Total loan amount.
Property Value: Value of the property being mortgaged.
Loan-to-Value Ratio: Ratio of the loan amount to the property value.
Employment Status: Borrower's employment status.
Payment History: History of loan payments.
Economic Indicators: Various macroeconomic factors like GDP growth, unemployment rate, etc.
Default Status: Target variable indicating whether the borrower defaulted (1) or not (0).
Steps in the Model Development
1. Data Preprocessing
Handling Missing Values: Missing values in economic indicators were filled using the forward fill (ffill) method.
Feature Scaling: All numerical features were scaled to ensure fair contribution to the model.
Encoding Categorical Variables: Categorical variables were encoded appropriately.
Exploratory Data Analysis (EDA): Performed to understand data distributions, correlations, and potential outliers.
2. Feature Engineering
Debt-to-Income (DTI) Ratio: Calculated to assess the borrower's debt relative to income.
Credit Utilization: Removed due to redundancy.
Economic Stress Indicator: Derived using Principal Component Analysis (PCA) on macroeconomic factors like GDP growth, unemployment rate, interest rate, and inflation rate.
Credit History Relative to Loan Issue Date: Derived to evaluate the relevance of the borrower's credit history to the loan.
3. Feature Selection
A custom function remove_highly_correlated_features was implemented to remove features with a correlation greater than 0.8, ensuring that only the most impactful and independent features were retained.
4. Model Development
Implemented the following models to predict mortgage default risk:

Logistic Regression
Random Forest Classifier
XGBoost Classifier
(Optional Advanced) Neural Network
5. Model Evaluation
The models were evaluated using the following metrics:

Precision: The proportion of true positives among all positive predictions.
Recall: The proportion of true positives among actual positives.
ROC-AUC Curve: Measures the model’s ability to distinguish between default and non-default.
Confusion Matrix: A matrix to visualize true vs. predicted classifications.
Feature Importance: Analyzed to understand the most influential features in the prediction.
6. Advanced Features
Cross-Validation: Applied to ensure the models' robustness.
Model Interpretability Report: Generated to provide insights into how models make predictions.
Risk Scoring Mechanism: Developed for quantifying default risk.
Business Recommendations: Provided actionable insights to improve business decisions.
Requirements
Python 3.x
Pandas
Scikit-learn
XGBoost
Matplotlib
Seaborn
NumPy
How to Run
Clone this repository.
Install the required libraries:
Copy code
pip install -r requirements.txt
Run the Jupyter notebook credit_risk_modeling.ipynb to execute the model and see results.
Conclusion
This project demonstrates the process of building a mortgage default risk prediction model, from data preprocessing and feature engineering to model development and evaluation. The final model can help in assessing the likelihood of mortgage defaults and provide insights for financial decision-making.
