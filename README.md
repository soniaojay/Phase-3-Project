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
The dataframe used entails SyriaTel customer usage pattern and their churn status from [Kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). The data included ~The dataset has 3,333 customers and 20 columns with no null values and a mix of data types. The data include:
The Target or Dependent Variable: 
**Churn**: the number of existing customers who may leave the service provider over a given period.
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
