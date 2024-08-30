# SyriaTel Customer Churn Prediction and Analysis

![image](Telecommunications.jpg)

This repository contains an analysis of customer data from Syriatel to provide insights into factors that contribute to customer churn. 

## Project Overview
In this project, I developed a predictive model to identify customers who are likely to churn from Syriatel, a telecommunications company. By analyzing customer behavior and service usage patterns, I aimed to help Syriatel proactively retain at-risk customers, thereby reducing revenue loss and improving customer satisfaction.

## Business Understanding
### Stakeholder Audience
The primary stakeholders for this project are the marketing and customer service teams at Syriatel. These teams are focused on understanding why customers leave and how to prevent churn. Additionally, the insights are valuable to the executive team for strategic decision-making and resource allocation.

### Dataset Choice
The dataset used for this project includes various customer attributes such as service usage, billing information, customer service interactions, and whether the customer has churned. These features are critical for understanding customer behavior and predicting churn. The dataset was sourced from![Kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset) and contains 3,333 rows and 21 columns.

## Data Understanding
The dataset includes the following features:

State: The state in which the customer resides.
Account Length: The duration (in days) the customer has had an account.
Area Code: The area code of the customer's phone number.
Phone Number: The customer's phone number (non-informative for modeling).
International Plan: Whether the customer has an international calling plan (yes or no).
Voice Mail Plan: Whether the customer has a voice mail feature (yes or no).
Number Vmail Messages: The number of voice mail messages the customer has.
Total Day Minutes: Total minutes the customer has used during the day.
Total Day Calls: Total number of calls made daily.
Total Day Charge: Total charges incurred during the day (derived from minutes).
Total Eve Minutes: Total minutes the customer has used during the evening.
Total Eve Calls: Total number of calls made during the evening.
Total Eve Charge: Total charges incurred during the evening (derived from minutes).
Total Night Minutes: Total minutes the customer has used during the night.
Total Night Calls: Total number of calls made during the night.
Total Night Charge: Total charges incurred during the night (derived from minutes).
Total Intl Minutes: Total minutes used for international calls.
Total Intl Calls: Total number of international calls made.
Total Intl Charge: Total charges incurred for international calls (derived from minutes).
Customer Service Calls: Number of calls made to customer service.
Churn: The target variable, indicating whether the customer churned (True) or not (False).

## Data Preparation
### The datasets were cleaned. Steps included:
1. Handling missing values and outliers.
2. Correcting data types as needed.
3. Ensuring that the data is ready for modeling.

## Data Analysis
### The analysis addressed the following key questions:
1. What are the primary factors driving customer churn at SyriaTel?
2. How accurately can we predict which customers are at risk of churning?
3. What features most strongly influence customer churn, and how can they be used to improve retention strategies?
4. How can SyriaTel leverage these insights to reduce churn and improve customer satisfaction?

## Results
### Key Findings
1. Frequent Customer Service Interactions Lead to Higher Churn: The number of customer service calls was identified as the most significant predictor of churn. 

2. High Day-Time Usage and Charges Correlate with Churn: Customers with higher usage during the day, leading to increased charges, are more likely to churn. 

3. International Plan Subscribers Are at Higher Risk: The analysis found that customers with international plans are more likely to churn, possibly due to the perceived value or cost of these plans.

4. Model Performance: The Random Forest model proved to be the most effective in predicting churn, with an accuracy of 96.0%, a precision of 95.7%, and an AUC-ROC score of 0.91.

## Visualizations
### Correlation Analysis
![Correlation Analysis](images/correlation_analysis.png)
Correlation Analysis will help us identify which features may be most influential in predicting customer churn.

### Univariate Analysis
![Univariate Analysis](images/univariate_analysis.png)
Univariate Analysis helps to compare the usage patterns (total day minutes) between customers who churn and those who do not. This type of analysis is exploratory as it gives insights into how customer behavior (in terms of usage) might be linked to their decision to stay or leave.

### Bivariate Analysis
![Bivariate Analysis](images/bivariate_analysis.png)
Bivariate analysis explores the relationship between two variables: "customer service calls" (independent variable) and "churn" (dependent variable). The analysis examines how the churn rate varies with different levels of customer service calls.

## Modeling
I employed several machine learning models to predict customer churn, including Logistic Regression, Decision Tree, Random Forest, and Support Vector Machines (SVM). After evaluating their performance, the Random Forest model was selected as the final model due to its high accuracy, precision, and recall scores.

### Feature Engineering
I created additional features such as total minutes, average call duration, and interaction terms to capture more customer behaviors. These features were crucial in improving model performance.

### Hyperparameter Tuning
To ensure optimal model performance, I applied hyperparameter tuning techniques to the Random Forest model. This process involved adjusting key parameters such as the number of trees, maximum depth, and minimum samples per split. The tuning resulted in a well-calibrated model that effectively balanced accuracy, precision, and recall, making it highly suitable for predicting customer churn.

## Evaluation
The Random Forest model was evaluated using various metrics:

Accuracy: 96.0%
Precision: 95.7%
Recall: 75.9%
F1 Score: 84.6%
AUC-ROC: 0.91

These metrics demonstrate the model's ability to accurately predict customer churn, with a particular focus on minimizing false negatives (i.e., failing to identify customers who will churn).

## Conclusion
The analysis identified key factors contributing to customer churn, such as the number of customer service calls and high day-time usage. By addressing these factors, Syriatel can improve customer retention. The Random Forest model provides a reliable tool for identifying at-risk customers, enabling proactive retention strategies that can lead to significant cost savings.

## Next Steps
Implementation: Deploy the model in a live environment to continuously monitor and predict customer churn.

Actionable Insights: Use the insights from the model to enhance customer service interactions and offer personalized retention plans to high-risk customers.

Further Analysis: Explore additional features and data sources to refine the model further and ensure it adapts to changing customer behaviors.

## Links
- [Canva Presentation](https://www.canva.com/design/DAGPSgnehuo/DjR5vqgN-jziOU7GWlqk5g/edit?utm_content=DAGPSgnehuo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)


