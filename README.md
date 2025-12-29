Project Name: Customer Churn Prediction 

Description
This project focuses on predicting customer churn and understanding why customers leave.
The goal is not only to build a predictive model, but also to translate predictions into
clear business actions that help reduce churn.

Dataset
The dataset contains customer-level data with the following types of features:
- customer_id
- churn (0 = stays, 1 = leaves)
- contract type
- payment method
- monthly charges
- total charges
- tenure
- usage level
- last login days
- complaints
- promo status
- region
- customer segment

The dataset is clean and ready for modeling.

EDA (Exploratory Data Analysis)
We analyzed the data to understand churn behavior:
- overall churn vs non-churn ratio
- churn by contract type, payment method, and customer segment
- distribution of numerical features
- differences between churned and non-churned customers

Key findings:
- Month-to-month contracts have the highest churn
- Shorter tenure is linked to higher churn
- Higher inactivity increases churn risk

Feature Engineering & Preprocessing
- Numerical features were scaled using StandardScaler
- Categorical features were encoded using OneHotEncoder
- A preprocessing pipeline was built to avoid data leakage

Train / Test Split
- Data was split into 80% train and 20% test
- Stratified split was used to preserve churn ratio

Modeling
Baseline model:
- Logistic Regression with class_weight='balanced'

The model was trained using a full preprocessing pipeline.

Evaluation
The model was evaluated using:
- Precision
- Recall
- ROC-AUC
- Confusion Matrix
- Threshold tuning

Results showed good separation between churn and non-churn customers,
with a strong recall score suitable for churn use cases.

Feature Importance
Model coefficients were analyzed to understand key churn drivers:
- Contract type
- Tenure
- Customer activity
- Auto-renewal status

Business-Oriented Churn Scoring 
Customers were ranked by predicted churn probability:
- Top 10% of customers accounted for a large share of total churn
- This enables focused retention strategies

Business Impact Simulation
A simple retention simulation was performed:
- Targeted top 20% high-risk customers
- Estimated saved customers and revenue
- Compared campaign cost vs value saved

Final Model
The final model was trained on the full dataset and saved for reuse.
It can be used to score new customers without retraining.

Conclusion
This project demonstrates a complete mid+ data science workflow:
- data analysis
- modeling
- evaluation
- explainability
- business impact

The focus is on real-world usability.
