#### *Company information and data has not been disclosed. However the code for this project including exploratory analysis and final recommendations for the company are included.*


### 1 Motivation:
A ride-sharing company is interested in predicting rider retention. To help explore this question, the company has provided a sample dataset of a cohort of users who signed up for an account.
The goal of this project is to understand what factors are the best predictors for retention, and offer suggestions to operationalize those insights to help the company.
We need to not only build a model that minimizes error, but also a model that allows you to interpret the factors that contributed to your predictions.

<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/10040565/22268501/682ae5b0-e24d-11e6-9f8a-0f270f3266df.jpg" width="400"/>
</p>

### 2 Project Scope:
1. Find key features in the data set that can help reduce churn.
2. Build a model that can predict churn given new user information.


### 3 Feature selection:
The predictor variable is not available in the dataset. However for a user we can define churn if that user has not been active for the last 30 days.
#### a. Phone type:
<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/10040565/22271300/60e14cb6-e259-11e6-9d48-d175b13dbae4.png" width="400"/>
</p>

As per the chart, **a high percentage of Android users have churned.** The company might want to look at the Android app to figure out why Android users are not as active as Iphone users.
