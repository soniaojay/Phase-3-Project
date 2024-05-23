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
  
## Modeling
To achieve the research goal of predicting customer churn, i first analyzed the existing churn rate in the dataset, which revealed a churn rate of 14.49%. With a clear understanding of the overall churn rate, aimed to pinpoint which features of a customer's phone plan are most influential in their decision to churn. After identifying these key features, my next step was to develop strategies to address them and reduce churn. Finally, this research sought to give recommendations and solutions before implementing them nationwide.

To build a classifier to predict whether a customer will churn from SyriaTel, three models were used to aid in the prediction:

- **Logistic Regression Model**
- **Decision Tree Model**
- **Random Forest Model**

Assessment of the all models was based on the accuracy score, precision, recall and F1 Score. However, i decided to emphasize the recall score as the main metric when assessing the prediction results of the models. As a telecommunications company with the aim of reducing customer churn, the recall score of each model was a more applicable metric as the aim to minimize the amount of false negative predictions. Maximizing the recall score will ensure that the model does not miss out on any potential customers who are likely to churn and leave the phone company.

## Results/Findings

Across all of the models listed above, Logistic Regression Model was the best model and the most appropriate model given its mix of high recall score and accuracy score on training data and testing data. The model achieved a recall of 81% for the negative class (False) and 78% for the positive class (True) with an accuracy of 80.4%. This indicates that the model is effective at capturing a substantial portion of the positive cases. 
![alt text](![download2](https://github.com/soniaojay/Phase-3-Project/assets/152200934/194bbb43-f7d8-4024-b39b-147c036c403c)

Moving forward with the Logistic Regression Model as the best model for predicting churn, i then identified the key features importances that impacted this model the most: total charge overall (both domestic and intl) and customer satisfation. The predicted overall churn rate after capping 'customer_call_satisfaction' at 0.72 was 25.50%. The increase from 14.49% to 25.50% indicates that the logistic regression model, after capping the satisfaction scores, predicts a significantly higher number of customers will churn. Feature Influence: This suggests that the 'customer_call_satisfaction' feature has a substantial influence on the model's predictions. By capping it, the model might be overestimating the likelihood of churn because it loses granularity in satisfaction scores. The increased predicted churn rate could signal underlying issues in customer satisfaction or potential flaws in how the feature is engineered. Feature Engineering: Explore other ways to handle 'customer_call_satisfaction' without capping, such as using different thresholds or creating new interaction terms with other features.

Implementation of a fixed charge for those who go over 700 minutes at a price of $71.05. The logistic regression model was selected to be used here as the model had the best predictor for the training and testing data for the recall. After applying our fixed fee plan, churn decreased from 14.49% to 0. The predicted churn value of 0 indicates that, according to the model, the customer is not likely to churn. In other words, based on the features provided (including capped total minutes and charge per minute), the model suggests that the customer is expected to remain with the telecom service. This prediction could be valuable for decision-making processes related to customer retention strategies and resource allocation within the telecom company.

## Conclusion

In conclusion, leveraging our logistic regression model, we've gained insights into predicting customer churn and informing retention strategies for our telecom service. Firstly, by capping the customer_call_satisfaction feature at the 75th percentile (0.72), we observed a predicted overall churn rate of approximately 25.50%. This suggests that addressing factors contributing to lower customer satisfaction could substantially impact churn reduction.

Secondly, when capping total_minutes_overall at the 50th percentile (around 700 minutes) and implementing a charge of $71.05 per minute for usage beyond this threshold, our model predicts a churn value of 0, indicating that customers are unlikely to churn under these conditions. Implementing targeted strategies, such as fixed charges for excess usage, based on these insights can significantly contribute to customer retention efforts. However, continuous monitoring and adaptation of strategies remain crucial for maintaining customer satisfaction and loyalty amidst evolving preferences and market dynamics.

Next step is to Conduct further market research on pricing plans can be conducted across SyriaTel's main competitors. In order to further improve on lowering the churn rate across all customers, we would need to collect more data from users. One way to implement a next step is to conduct a customer satisfaction survey to pinpoint more specifically other areas that can be improved upon in order to provide better customer experiences for all SyriaTel users.
