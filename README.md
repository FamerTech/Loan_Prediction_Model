# Loan_Prediction_Model
Project Overview
This project develops a machine learning model to predict loan default based on various borrower and loan characteristics. The goal is to identify potential defaulting loans early to help financial institutions mitigate risks.

Dataset
The project utilizes the Loan_default.csv dataset, which contains detailed information about loan applicants and their default status.

Methodology
1. Data Preprocessing and Exploration
Missing Value Handling: Missing values in key categorical features (HasMortgage, HasDependents, LoanPurpose, HasCoSigner, Default) were identified.
Categorical Feature Encoding: All categorical features (e.g., MaritalStatus, Education, EmploymentType, LoanPurpose, HasMortgage, HasDependents, HasCoSigner) were converted into numerical representations using a replace strategy.
Feature and Target Separation: The dataset was split into features (X) and the target variable (y, representing 'Default' status).
Train-Test Split: The data was divided into training and testing sets to evaluate model performance on unseen data.
2. Model Training
Model: An XGBoost Classifier was chosen for its robust performance with tabular data and ability to handle categorical features. The model was initialized with random_state=2 and enable_categorical=True.

Training: The model was trained on the X_train and y_train datasets.
4. Model Evaluation
Accuracy: The model's performance was evaluated using accuracy_score on both the training and test datasets. The test accuracy achieved was approximately 88.5%.
5. Feature Importance
Feature importances were calculated and visualized to understand which factors contribute most significantly to the loan default prediction. 'Age' and 'InterestRate' were identified as among the most important features.
6. Prediction System
A prediction system was implemented to demonstrate how the trained model can be used to predict the default status for new input data.
7. Model Persistence
The trained XGBoost model was saved using pickle for future use, allowing for deployment without retraining.
Libraries Used
pandas
numpy
matplotlib
seaborn
scikit-learn (StandardScaler, train_test_split, LogisticRegression, RandomForestClassifier, accuracy_score)
xgboost (XGBClassifier)
