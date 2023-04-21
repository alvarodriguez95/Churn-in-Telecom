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
![Customer Churn Rate](http://localhost:8888/files/Images/Customer%20Churn%20Rate.png)

Specifically sought the churn rate from the customers with a voice-mail plan and customer service calls.

## Voice Mail Plan Model
![
403 people with no voice-mail decided to leave (16.72%).
80 people with a voice-mail plan decided to leave (8.68%).

## Churn rate by Customer Service Calls
![
Represents the frequency of customer service calls. Churned customers tend to have a higher number of service calls. Customer service may be a factor for customer retention.

# Models
Model                Accuracy   Precision  Recall     F1 Score  
Dummy Model          0.85       0.00       0.00       0.00      
Logistic Regression  0.85       0.49       0.18       0.26      
Decision Tree        0.88       0.64       0.46       0.53      
KNN                  0.87       0.66       0.29       0.40      
Final Model          0.93       0.79       0.69       0.74      

# Final Model
![
Based on the classification reports, the final model performs better than the dummy model in terms of accuracy, precision, and F1 score. The final model has higher accuracy (0.93) than the dummy model (0.85), indicating that it correctly classifies more instances. 
The precision of the final model (0.73) is higher than that of the dummy model (0.00), indicating that the final model is better at identifying true positives. 
The recall of the final model (0.55) is higher than that of the dummy model (0.00), indicating that the final model is better at correctly identifying all positive instances. 
The F1 score of the final model (0.63) is higher than that of the dummy model (0.00), indicating that the final model strikes a better balance between precision and recall.
In summary, the final model is better than the dummy model across all metrics.

# Conclusion
In order to decrease customer churn rate from SyriaTel, SyriaTel should:
- Improve customer service as customer service calls were a significant predictor for churn rate
- Improve product offerings as customers who had a voicemail plan were less likely to leave
- Improve customer incentives as customers who stayed with Syria Tel for a significant time were less likely to leave

# Next Steps
- Run further models for a better scores
- Include further categories that were not used such as:
 - Social media behavior
 - Purchase behavior
 - Competitor analysis

# For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/alvarodriguez95/Churn-in-Telecom/blob/main/SyriaTel_Churn_Model.ipynb) or review the [presentation](https://github.com/alvarodriguez95/Churn-in-Telecom/blob/main/SyriaTel_Churn_Presentation.pdf).
