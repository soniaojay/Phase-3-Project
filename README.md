![alt text](https://www.telecomreviewafrica.com/images/stories/2022/06/Telecom_and_E-Business_Systems_Unlimited_Growth.jpg)

# From Satisfied Subscribers to Silent Exits: Unveiling Customer Churn Patterns at SyriaTel with Machine Learning.
## Table of Contents
- Business Overview
- Business Problem
- Data Understanding
- Analysis
- Results
- Conclusions
- Next Steps
- Repository Structure
  
## Business Overview
The telecommunications industry is a highly competitive landscape where customer retention plays a crucial role in a company's success. Customer churn, defined as the loss of subscribers to a competitor or service termination, poses a significant financial challenge for telecommunications companies. SyriaTel, a leading telecommunications provider, is no exception. To maintain a competitive edge and minimize revenue loss, SyriaTel requires a robust system to predict customer churn and implement targeted retention strategies.
The loss of subscribers to competitors or service termination, is a major financial concern for SyriaTel. This research proposal outlines a plan to develop a machine learning classifier that can predict customer churn with high accuracy. By identifying customers at risk of churning, SyriaTel can proactively implement targeted retention strategies, minimizing revenue loss and maximizing customer lifetime value.

## Business Problem
Customer churn is a significant financial burden for telecommunications companies like SyriaTel. The inability to accurately predict churn hinders the development of effective retention strategies.Churn rate is very important because it is typically more expensive to obtain new customers than to retain existing customer. This research aims to address this problem by building a machine learning classifier to predict customer churn for SyriaTel inorder to improve their churn rate.

## Data Understanding
The dataframe used entails SyriaTel customer usage pattern and their churn status from [Kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). 
The data included ~The dataset has 3,333 customers and 20 columns with no null values and a mix of data types. 
The data include:

The Target or Dependent Variable: **Churn**: the number of existing customers who may leave the service provider over a given period.

Predictors or Independent Variables: 
- account length: the number of days the user maintains a phone plan account.
- area code: the region where the user is located.
- international plan: "yes" if the user has the international plan, else "no".
- voice mail plan: "yes" if the user has the voice mail plan, else "no".
- number of voice mail messages: the number of voice mail messages the user has sent.
- total day minutes used: total number of minutes the user has been in calls during the day.
- day calls made: total number of calls the user has completed during the day.
- total day charge: total amount of money the user was charged by the Telecom company for calls made during the day.
- total evening minutes: total number of minutes the user has been in calls during the evening.
- total evening calls: total number of calls the user has completed during the evening.
- total evening charge: total amount of money the user was charged by the Telecom company for calls made during the evening.
- total night minutes: total number of minutes the user has been in calls during the night.
- total night calls: total number of calls the user has completed during the night.
- total night charge: total amount of money the user was charged by the Telecom company for calls made during the night.
- total international minutes used: total number of minutes the user has been in international calls.
- total international calls made: total number of international calls the user has made.
- total international charge: total amount of money the user was charged by the Telecom company for international calls made.
- number customer service calls made: number of customer service calls the user has made.
  
## Analysis
To achieve the research goal of predicting customer churn, i first analyzed the existing churn rate in the dataset, which revealed a churn rate of 14.49%. With a clear understanding of the overall churn rate, aimed to pinpoint which features of a customer's phone plan are most influential in their decision to churn. After identifying these key features, my next step was to develop strategies to address them and reduce churn. Finally, this research sought to give recommendations and solutions before implementing them nationwide.

To build a classifier to predict whether a customer will churn from SyriaTel, three models were used to aid in the prediction:

- **Logistic Regression Model**
- **Decision Tree Model**
- **Random Forest Model**

Assessment of the all models was based on the accuracy score, precision, recall and F1 Score. However, i decided to emphasize the recall score as the main metric when assessing the prediction results of the models. As a telecommunications company with the aim of reducing customer churn, the recall score of each model was a more applicable metric as the aim to minimize the amount of false negative predictions. Maximizing the recall score will ensure that the model does not miss out on any potential customers who are likely to churn and leave the phone company.

## Results/Findings

Across all of the models listed above, we have identified that the Logistic Regression Model was the best model and the most appropriate model given its mix of high recall score and accuracy score on training data and testing data. The model achieved a recall of 81% for the negative class (False) and 77% for the positive class (True) with an accuracy of 80.5%. This indicates that the model is effective at capturing a substantial portion of the positive cases. 
![alt text](![download2](https://github.com/soniaojay/Phase-3-Project/assets/152200934/194bbb43-f7d8-4024-b39b-147c036c403c)

Moving forward with the Logistic Regression Model as the best model for predicting churn, i then identified the key features importances that impacted this model the most: international plan, charge per call per day and charge per call intl. To address the impact of total charge in relation to churn, we modified the charge per day feature and focused on the day segment of charge per minute (defined as charge_per_min_day) and found a cutoff threshold of 35 cents per minute for all customers who's total day minutes is 200 minutes. We identified 200 minutes as the 50th percentile and sought out to adjust all charge per mins to be capped at 35 cents for all customers making day calls over 200 minutes. After applying our suggested fixed fee plan, we saw that churn rate decreased from 14.49% down to 12.57%. To address the relationship between customer service calls and churn, we then identified a threshold of 0.72 that we seek to target as the ideal threshold. We then looked to create a theoretical scenario where call rate was fixed at 0.72 and a new fixed pricing fee of 35 cents per minute on calls over 200 minutes and found that churn rate improved and dropped down to around 9.81%.
