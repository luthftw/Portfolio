# TYB Bank's Customer Churn Prediction Project Overview
- The model was built to help TYB Bank to predict which customers were churning, and how to stop the churning process
- This dataset is obtained from https://www.kaggle.com/sakshigoyal7/credit-card-customers
- The data was cleaned, by Remove CLIENTINUM (customers ID) as a unique identifier, and 0 replace 'unknown' values found in customers’ profile, by modes
- Engineered features Gender and Marital Status features are modified with one-hot encoding, and other categorical features modified with label encoding
- Train model with 5 different algorithms, and choose the top 3 for next hyperparameter tuning
- Handle imbalanced class with scale_pos_weight(only for XGBoost)
- Validate the model with data test

### Existing Problem
TYB Bank is struggling to improve customers’ churn-rate on their credit card services.

### Improvement Needed
Prediction modelling for which customer is likely to churn, and Proactive Reengagement to approach customer to stay in their services.

### Business Impact/Purpose
Preventing profit loss from Customers’ churn and increasing company’s revenue.

# Insight From the Data
![image](https://user-images.githubusercontent.com/83952278/123299142-69d4a200-d543-11eb-9a61-5ace501d6904.png)
Insight :
- Profil pengguna produk kartu kredit yang terbagi menjadi 5 kategori, dimana fokusan dari model kali ini akan membahas pada 
- Dapat dilihat pada background marital status dan income category, terdapat nilai ‘unknown’ yang akan kita proses di data-preprocessing.




