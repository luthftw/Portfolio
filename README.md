# TYB Bank's Customer Churn Prediction Project Overview
- The model was built to help TYB Bank to predict which customers were churning, and how to stop the churning process
- This dataset is obtained from https://www.kaggle.com/sakshigoyal7/credit-card-customers
- The data was cleaned, by Remove CLIENTINUM (customers ID) as a unique identifier, and 0 replace 'unknown' values found in customers’ profile, by modes
- Engineered features Gender and Marital Status features are modified with one-hot encoding, and other categorical features modified with label encoding
- Train model with 4 different algorithms, and choose the top 1 for next hyperparameter tuning(XGBoost)
- Validate the model with data test

### Existing Problem
TYB Bank is struggling to improve customers’ churn-rate on their credit card services.

### Improvement Needed
Prediction modelling for which customer is likely to churn, and Proactive Reengagement to approach customer to stay in their services.

### Business Impact/Purpose
Preventing profit loss from Customers’ churn and increasing company’s revenue.

# Insight From the Data
**1.**

![image](https://user-images.githubusercontent.com/83952278/123299142-69d4a200-d543-11eb-9a61-5ace501d6904.png)
Insight :
- User profiles for credit card products are divided into 5 categories, where the focus of this model will be on 'Card Category'
- There are 4 different categories in 'Card Category' user profile, but, 93% of the data is in `Blue Card` category
- In the background of marital status and income category, there is a value of `Unknown` which will be processed in data-preprocessing.


**2.**

![image](https://user-images.githubusercontent.com/83952278/123448298-f72bfb00-d604-11eb-8f31-51ff6b153b8c.png)

Insight :
- 93% profit loss comes from 1,519 blue card holders churned customers, which dominating by having more than 90% customers in blue card only
- The huge gap between blue card and other categories are the reason we need to focus to pick up from blue card holders

**3.**

![image](https://user-images.githubusercontent.com/83952278/123448447-1f1b5e80-d605-11eb-81f4-4ab8c08eaa87.png)

Insight :
- Despite having the largest user, blue card category is considerably low on transactions rather than any other cards
- Blue card users only spends 29% from his credit card limit per year, meaning that we can still push to generate more spending to prevent churning

**4.**

![image](https://user-images.githubusercontent.com/83952278/123514705-7598a380-d6be-11eb-9700-6b789c17724b.png)

Insight :
- Customers owning only 1 or 2 products still likely to compare TYB Bank with other Banks or Credit Card services, and the ore likely they are from churning
- Although in numbers, churn in the third products are pretty high, the number of existing or happy customers are also high

**5.**

![image](https://user-images.githubusercontent.com/83952278/123514930-88f83e80-d6bf-11eb-8a3d-5414120db866.png)

Insight :
- The more frequent customers contacting customers support, the more likely they are from churning
- For more than 2,500 customers or  are contacting customers’ support 2-3 times, meaning that TYB Bank needs to improve the customers’ support service immediately to make their customers satisfied and not churning



# Data Modelling
 <table>
 <thead>
  <tr>
   <th>Model</th><th>Recall</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Decision Tree</td><td>77%</td>
  </tr>
  <tr>
   <td>Random Forest</td><td>77%</td>
  </tr>
  <tr>
   <td>XGBoost</td><td>91%</td>
  </tr>
  <tr>
   <td>ADABoost</td><td>83%</td>
  </tr>
 </tbody>
</table>
 
 
Recall is used to prevent incorrectly predicting ‘churn’-ed customers as’ not churn’. Meanwhile, its ok to engage with those who are mistakenly tagged as 'not churned'. It could potentially make them even happier. The `Train Recall Score` is about 98% and the `Test Recall Score` is about 91% 

# Business Insight and Recommendation
Based on our focus in the `Blue Card Category`, some aspects that affect their churning process are; low on transactions, number of products owned by customers, and how frequent the customers contacting CS. From these aspect, These are our recommendation:

1. Cashback Rewards
To attract more customers and prevent customers from inactivity, giving cashback rewards is one of our recommendation. There are terms and conditions to apply, so the cashback rewards still making profit to the TYB Bank.
2. Customer Relationship & Customer Support Improvement
From the aspect of the frequencies of customers contacting customer support, we recommending to give training  for customer relationship, also improving relationship from CS to the customer. The aspect that could be improved are number of products owned by customers and inactivity by customers


# Team Behind This Project
As the final project to finish Data Science program in Rakamin Academy, this model was built with a team consisted by 5 member, called GGS (including me)
 <table>
 <thead>
  <tr>
   <th>Member</th><th>Linkedin</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Mentor: Stephanie</td><td>https://id.linkedin.com/in/stephanie-stephanie</td>
  </tr>
  <tr>
   <td>Muhammad Luthfi (me)</td><td>https://www.linkedin.com/in/luthftw/</td>
  </tr>
  <tr>
   <td>Marteen Joshee Octavian</td><td>https://www.linkedin.com/in/marteen-joshe-o-156a111bb/</td>
  </tr>
  <tr>
   <td>Salman Tulus Pribadi</td><td>https://www.linkedin.com/in/salman-pribadi/</td>
  </tr>
  <tr>
   <td>Rama Satriya</td><td>https://www.linkedin.com/in/ramasatriya/</td>
  </tr>
 </tbody>
</table>
 
 

