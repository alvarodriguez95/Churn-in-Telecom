# Churn-in-Telecom
![Telecommunications](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSuYnpLhQOEdyYKHPScIVzt8uVSVQIiixwXZA&usqp=CAU)

Phase 4: Alvaro Rodriguez

# Overview
For this project, we will be using logistic regression, decision tree, and knn modeling to analyze the features used to determine the churn rate of customers in SyriaTel, a Telecommunications company.

# Business Problem
![
I have been contracted by the VP of Customer Service to help improve customer churn rate and entice customers to stay at SyriaTel. SyriaTel has been losing customers in the previous months and they are eager to retain these customers. They also want to see the best predictors in retaining these customers and reducing customer churn rate.

# Data & EDA
Data regarding customer churn rate was retained from SyriaTel's database in Kaggle.com. Our primary dataset contained about 3333 customers that use SyriaTel.
Database is [here](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset).

Created a target column based on churn rate and split it into numerical and categorical features. 
False means that customers did not leave (85.51%).
True means that they did leave (14.49%).
![Customer Churn Rate](data:image/png;base64,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)
Specifically sought the churn rate from the customers with a voice-mail plan and customer service calls.

## 
# Models

# Final Model
