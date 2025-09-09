📊 Customer Attrition (Churn) Prediction
   Predicting customer churn (attrition) in the telecom sector using machine learning, with techniques for data preprocessing,
    feature engineering, handling class imbalance, and model benchmarking.


🚀 Project Overview
   Customer churn is a critical business problem in the telecom industry — retaining existing customers is more cost-effective than acquiring new ones.
   This project builds a complete end-to-end ML pipeline to identify customers likely to churn, using the Telco Customer Churn dataset.

📂 Dataset
Source: [Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
```
  Size: 7,043 rows × 21 columns
  Target Variable: Churn (Yes = customer left, No = retained)
  Features include:
  Demographics (gender, senior citizen, dependents)
  Services (phone, internet, streaming, security)
  Billing & Contracts (tenure, monthly charges, payment method, contract type)
```
```
🛠️ Tech Stack
   -Python Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn (SMOTE), XGBoost
   -ML Techniques:
      -Data Preprocessing (missing values, label encoding, scaling)
      -Feature Engineering & Selection (Correlation, Chi-Square, ANOVA F-test)
      -Class Balancing (SMOTE oversampling)
      -Model Training & Evaluation

📊 Workflow
   1.Data Preprocessing
      -Removed irrelevant columns (customerID)
      -Handled missing values in TotalCharges
      -Label encoding for categorical features
      -Normalization for skewed numerical features
    2.Handling Class Imbalance
      -Original dataset: 73% Not Churn vs 27% Churn
      -Applied SMOTE → Balanced dataset: 5174 (Not Churn) vs 5174 (Churn)
    3.Feature Selection
      -Dropped weakly correlated features (e.g., gender, PhoneService, StreamingTV)
      -Retained all numerical features (tenure, MonthlyCharges, TotalCharges)
    4.Exploratory Data Analysis (EDA)
      -Higher churn for:
         -Month-to-month contracts
         -Electronic check payment method
         -Customers with high monthly charges & low tenure
      -Lower churn for:
         -Long-term contracts (1/2 years)
         -Customers with partners or dependents
    5.Model Training & Evaluation
      -Implemented multiple models and compared performance:
         -----------------------------------------------------------------------
         |         Model       | Accuracy  | ROC-AUC   | Notes                 |
         | ------------------- | --------- | --------- | --------------------- |
         | **XGBoost**         | **85.6%** | **93.9%** | Best performer        |
         | Random Forest       | 81.1%     | 89.8%     | Good generalization   |
         | Decision Tree       | 78.8%     | 85.9%     | Simple, interpretable |
         | Logistic Regression | 77.4%     | 84.6%     | Baseline model        |

```
```
📈 Visualizations
      -Churn distribution (pie chart & countplot)
      -Categorical features vs churn (bar plots)
      -Numerical distributions (tenure, monthly charges, total charges)
      -Correlation heatmap with target variable
      -Confusion matrix heatmap with precision/recall metrics
```
```
📦 How to Run
   -Clone the repository
      -git clone https://github.com/your-username/customer-churn-prediction.git
      -cd customer-churn-prediction
   -Install dependencies
      -pip install -r requirements.txt
    -Run Jupyter Notebook or Python scripts
      -jupyter notebook churn_prediction.ipynb

📌 Key Insights
   -Customers on month-to-month contracts and using electronic check payments are most likely to churn.
   -Customers with higher tenure and long-term contracts are less likely to churn.
   -XGBoost outperformed all other models with the highest accuracy and ROC-AUC.
```
