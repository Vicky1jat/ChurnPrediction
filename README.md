📊 Customer Attrition (Churn) Prediction
   Predicting customer churn (attrition) in the telecom sector using machine learning, with techniques for data preprocessing,
    feature engineering, handling class imbalance, and model benchmarking.


🚀 Project Overview
   Customer churn is a critical business problem in the telecom industry — retaining existing customers is more cost-effective than acquiring new ones.
   This project builds a complete end-to-end ML pipeline to identify customers likely to churn, using the Telco Customer Churn dataset.

📂 Dataset
Source: [Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
  Size: 7,043 rows × 21 columns
  Target Variable: Churn (Yes = customer left, No = retained)
  Features include:
  Demographics (gender, senior citizen, dependents)
  Services (phone, internet, streaming, security)
  Billing & Contracts (tenure, monthly charges, payment method, contract type)

⚙️ Project Workflow (ML Pipeline)
   🛠️ Tech Stack
      -Python Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn (SMOTE), XGBoost
      -ML Techniques:
         -Data Preprocessing (missing values, label encoding, scaling)
         -Feature Engineering & Selection (Correlation, Chi-Square, ANOVA F-test)
         -Class Balancing (SMOTE oversampling)
         -Model Training & Evaluation
