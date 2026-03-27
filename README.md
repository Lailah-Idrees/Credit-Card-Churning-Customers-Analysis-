# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Credit Card Churn Predictions Analysis 
Bank Churners Dataset Analysis is a comprehensive data analysis tool designed to streamline data exploration, analysis, visualisation and machine learning. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# Dataset Content #
This dataset contains Credit Card Churn for individuals at a bank, along with key behavioural and demographic attributes. The dataset consists of 10127 rows and 20 columns. Three columns were removed as they were deemed not neccessary for analysis these are: Client number and two Naive bayes Clasifier columns.
The Data was sourced from Kaggle link [here](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)

A List of the all the variables is listed below with an explaination of what they show:

# Target

**Attrition_Flag** - Indication of a customer leaving or staying on the credit card services

# Features

**Customer Age**

**Gender**

**Dependent_Count** - How many dependents the customer

**Education Level**

**Marital Status**

**Income Category**

**Months On Book** - How long the customer has been using the credit card service

**Total Relationship Count** - Number of products the customer has with the bank (e.g., savings, loans, credit card).

**Months Inactive 12 mon** - Number of months (in the last 12) where the customer had no activity.

**Contacts Count 12 mon** - How many times the customer contacted the bank in the last 12 months

**Credit Limit** - Maximum credit available on the card

**Total Revolving Balance** - Amount the customer is carrying month‑to‑month (not paid off)

**Avgerag Open To Buy** - Credit_Limit minus Total_Revolving_Bal. Essentially: how much credit they still have available.

**Total_Amt_Chng_Q4_Q1** - Change in total transaction amount from Q1 to Q4. Measures spending trend (increasing or decreasing).

**Total_Trans_Amt** - Total amount spent in the last 12 months

**Total_Trans_Count** - Total number of transactions in the last 12 months

**Total_Ct_Chng_Q4_Q1** - Change in transaction count from Q1 to Q4

# PowerBI Dashboard
The link to the Stroke Predictions Dashboard can be found [here](https://app.powerbi.com/groups/me/reports/201c3c20-d4f5-4ad2-a4cf-85f793f579cd/a7838fd6db23880af7fa?experience=power-bi)

# Project Plan
* Load and Clean data: Removing outliers, encoding categorical data, identifying and dealing with missing or duplicated values
* Condcut visualisations on data to identify relationships between the target and features
* Conduct multiple Machine learning optimisation using Hyperparameter optimisation and Pipeline optimisation 
* Construct a comprehensive and easy to follow PowerBI Dashboard to present the most relevant data

# Hypothesis

**H1. Relationship between months on the books and attrition**
Customers who have been with the bank for a longer period (“months on book”) will be more likely to remain as existing customers. Longer time on the books typically reflects stronger loyalty, deeper familiarity with the institution, which should reduce the likelihood of attrition.

**H2. Relationship between credit limit and attrition** 
Customers with higher credit limits will be less likely to attrit. Higher limits often indicate better credit scores and a more established relationship with the bank, which may increase satisfaction and reduce the incentive to leave.

**H3. Relationship between product holdings and attrition**
Customers who hold multiple products with the bank (e.g., credit cards, savings accounts, loans) will be more likely to stay. Having several accounts increases dependency on the institution and raises the effort required to switch providers, thereby lowering attrition risk.

**H4. Gender differences in attrition**
There will be little to no difference in attrition rates between male and female customers. Gender is not expected to be a meaningful predictor of churn.

**H5. Relationship between age and attrition**
Older customers will be more likely to remain as existing customers. Age is associated with greater financial stability and stronger long-term relationships with financial institutions, which may reduce the likelihood of switching banks.

# Reflection

**Data privacy and responsible handling**
The dataset contains customer‑level financial information, which requires careful management even when used only for analytical purposes. To comply with GDPR and general data‑protection principles, all personally identifiable was removed unless it is strictly necessary for the analysis. Customer ID numbers were excluded from the dataset because they were not required for modelling and could potentially be used to re‑identify individuals. Removing this field aligns with the GDPR principle of data minimisation, which states that only essential data should be processed. The analysis therefore uses only anonymised, non‑identifiable attributes to ensure customer privacy is protected.

**Bias and representativeness**
Although the project focuses on understanding attrition behaviour rather than making decisions that directly affect customers, bias can still influence the insights produced. Therefor the ML Model would be considered low-risk, there is low societal impact and low risk of harm. If the model learns patterns that reflect historical inequalities or imbalances in the dataset, the resulting insights may be misleading. This is particularly relevant for a bank manager who may use the findings to invest in retention strategies  biased insights could lead to ineffective interventions or misallocation of resources.

The dataset is imbalanced, with significantly more existing customers than attrited customers. This imbalance can cause the model to favour the majority class, reducing its ability to detect true attrition patterns. This is most likely one of the contributing factor to why the ML was overfiited to the test data. Ideally, additional data on attrited customers would be collected to improve representativeness. Prior to modelling, the dataset was cleaned and checked for inconsistencies, and demographic distributions were reviewed to ensure no obvious skew that could distort the analysis.

**Fairness and potential impact**
Although the model is not used to approve credit or make decisions that directly affect customers, fairness still matters. If demographic variables such as gender, age, or socioeconomic background were incorrectly interpreted as drivers of attrition, the bank could unintentionally target or overlook certain groups. This would not only be ethically problematic but also operationally inefficient.

The analysis found that demographic variables had minimal predictive power, reducing the risk of demographic bias influencing conclusions

# Challenges
The most significant challenge in this project was the uneven distribution of attrited versus existing customers. The dataset contained far fewer attrited customers, which made it difficult for the machine‑learning model less accurate. The training and test sets may not have reflected the same imbalance, leading to the model becoming biased toward predicting the majority class, leading to inflated training performance and weaker generalisation on unseen data. This imbalance likely contributed to the overfitting observed in the model results, where training accuracy was extremely high but test performance dropped noticeably.

Another challenge was the large number of features included in the dataset, many of which offered little value for predicting attrition. Several demographic variables showed minimal correlation with churn and added noise rather than insight and just extended the timeline of analysis


