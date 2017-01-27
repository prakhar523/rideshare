# Ride Share Case Study

#Intro 

This case study was done as part of the Data Science Immersive program at Galvanize. My partner Cynthia and I were given 7 hours to:
  - Analyze data from ride share "Company X" 
  - Prepare a presentation for "Company X"

#The Problem

Company X is interested in predicting rider retention. Identify what factors are the best predictors for retention, and offer suggestions to operationalize those insights to help Company X. 

#The Target

The target was to analyze churn rates for Company X. A customer is pronounced "inactive" or "churned" if they have not used the service in the last 30 days. 

#Exploratory Data Analysis

Number of records: 50,000
Inactive customers:   30777 - 61%
Active customers   19223 - 39%

Data limited to 3 cities

Columns with NaN values:
Avg_rating_by_driver (201) – replaced with average of column
Avg_rating_of_driver (8122) - replaced with average of column
Phone (type) – (396) replaced with ‘Unknown’
 
#Model Selection

Random Forests proved to be most appropriate to model churn prediction based on accuracy, precision, and recall. This model was chosen over Logistic Regression, Decision Tree, SVM, and Naive Bayes. 
 
![Model Selection](/model_choosing.png?raw=true "Choosing a Model")

###Tuning The Model

The following graphs were used to tune the parameters of the Random Forests model.
![Model Tuning](/rf_parameters.png?raw=true "Tuning Our Model")

#Findings

The first major divide in the data was seen between cities. One city showed two times more active users the other two. Next we tracked feature importances in the Random Forests model. This showed which features most polarized the active group vs. the inactive group.

![Model Tuning](/city_differences.png?raw=true "Tuning Our Model")

