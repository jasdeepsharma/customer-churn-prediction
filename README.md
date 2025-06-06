**Customer Churn Prediction Project**
This project focuses on predicting customer churn using machine learning models on the Telco Customer Churn dataset. It demonstrates a complete data science pipeline including data preprocessing, exploratory data analysis, feature engineering, model training, and evaluation.

**Problem Statement**
Customer churn is a major concern for subscription-based businesses. The goal of this project is to use historical customer data to predict whether a customer is likely to leave the company (churn), helping the business take proactive retention measures.

**Dataset**
Source: Telco Customer Churn dataset (Kaggle)

**Target Variable:** Churn (Yes / No)

Features include customer demographics, account information, services subscribed, and payment methods.

**Class Distribution**
As seen in the plot below, the dataset is imbalanced:
![{835275CC-A744-402A-B23E-5F50FE69011E}](https://github.com/user-attachments/assets/817a7bd3-694e-4ad4-a7ae-3a99add02e4d)


Non-churned: ~5,100

Churned: ~1,900


**Exploratory Data Analysis (EDA)**
Visualized churn distribution, contract types, internet service impact, and monthly charges.

Handled missing values and encoded categorical variables using one-hot encoding.

**Machine Learning Models Used**
Three classification models were built and compared:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

Each model was trained on the same train-test split and evaluated using classification metrics and ROC AUC.

**Evaluation Metrics**
      Model	           Accuracy	  Precision (Churn)	  Recall (Churn)	  ROC AUC
Logistic Regression	    0.78	        0.62	            0.49	            0.83 
Random Forest	          0.79	        0.64	            0.49	            0.81
XGBoost	                0.78	        0.60	            0.51	            0.81

Logistic Regression surprisingly had the highest ROC AUC in this case, showing that simpler models can perform well without tuning.

**ROC Curve for XGBoost**

![{8FBB7069-F591-48F0-8694-114D1B50A88B}](https://github.com/user-attachments/assets/a1153a3d-fcd9-4464-98f3-c58244ead16a)

**Key Takeaways**
- Logistic Regression performed the best overall based on ROC AUC.
- XGBoost had slightly better recall than other models, making it useful in cases where identifying all churn cases is critical.
- All models struggled slightly due to class imbalance.

**Next Steps**
- Apply SMOTE or class weighting to handle imbalance
- Perform hyperparameter tuning (e.g., GridSearchCV)
- Experiment with feature selection and ensemble techniques

**Tech Stack**
- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- XGBoost
- Jupyter Notebook
