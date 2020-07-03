# Telecom-Churn

### Business Objective 
Telecom industry is a very competitive space, with easy and low cost of transition between different service providers. This results in high churn rates, that reach as high as 15-25%. While the consumer's cost of transition is less, it costs telecom companies 5-10x more to acquire new customers as compared to retaining them. Therefore, the objective of this analysis is to identifying patterns indicating a churn of a consumer. Using this insight the telecom company can effectively spend resources on retaining the profitable consumers
### Domain Understanding
1. Telecom models are divided into prepaid and postpaid. In case of postpaid, the customers inform the telecom companies about the churn however prepaid is harder to keep track of. Therefore, we will use test different model to identify key behavioural factors of these customers
2. The 80-20 is applicable in this industry as well. In the Indian and South Asian Market, 80% of revenue is accounted for by the top 20% customers.
3. Churn can be defined in 2 ways: revenue based and usage based
4. The customer lifecycle is divided into 3 phases:
    * Good Phase: this is the ideal phase where the client is using the service and is satisfied with the current provider
    * Action Phase: the competitive companies start poaching the clients, and the behaviour may stay fluctuating here. It is important to identify a churner in this stage and take preventive actions
    * Churn Phase: in this phase the consumers have already churned
### Model Development
1. Pre-Processing:
  * Filter the high value consumers. Select only the top 70% of customers
  * Data cleaning: 
      1. Delete columns with more than 75% null/zero values or 1 unique value
      2. Delete rows of columns with more than 75% null values
      3. Impute rows with null <10% and zero<25%
      4. Delete columns with zero values > 70%
      5. Analyse the columns with more than 50% null or zero values
        1. Delete column with null>50%
        2. Impute columns with null<1%
     6. Handle date objects:
        1. Remove null values
        2. Change format from string to int 
2. Data Preparation
    1. Tag Churners
    2. Remove attributes of churn phase
    3. Handle data imbalance
3. EDA
    1. Integer analysis
    2. Float analysis
    3. Identify Outliers
    4. Outlier Treatment
    5. Look for correlations
4. Modelling
    1. PCA - identify the people who will churn
    2. Model Selection (Use cross_val_score for model selection and evaluate the appropriate model using a box plot)
    3. Hyperparameter tuning for Logistic Regression
    4. Model Development and feature selection using RLE and manual selection
    5. Find the optimum Threshold for classification

### Evaluation
The final model achieved gives accuracy, sensitivity and specificity of about 82% and ROC area reaches as high as 89%

### Recommendation
Basis our analysis, we identified a set of 12 potential features responsible and indicating churn which covered the range of incoming calls, outgoing calls and data usage compared in month 6 and month 8

*Action Plan*

Constantly check the change in behaviour pattern across the months. Can look for a 20% reduction in behaviour wrt the 12 features. If there is a drop noticed in the usage, a telecom provider executive can call up the customer and discuss concerns and recommend plans
Also keeping in mind the heavy uage of data, cost effective data plans can be developed and sold to the users
