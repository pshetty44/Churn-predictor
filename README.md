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

#### b. First 30 days:
<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/10040565/22271301/60e56486-e259-11e6-9d30-d23144ce0cb7.png" width="400"/>
</p>

**On average, active users made 3.3 trips in the first month, compared to 1.65 trips for a non active user.** We can use this feature to predict if a user will churn or not in the future.

#### c. Luxury car user:
<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/10040565/22272225/7192b93c-e25e-11e6-8160-ad82426dbdd3.png" width="400"/>
</p>

**Luxury car users are more active(less churn) than regular car users.**

#### d. Churn rate by city:
<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/10040565/22271298/60dc81e0-e259-11e6-8f7c-587b7d9a4eba.png" width="400"/>
</p>

**King's Landing City has the highest ratio of active users compared to any other city.**


### 4 The model:
Several features were dropped due to various reason like correlation between features, leakage and due to the usage of dummy variables. Please refer to details in the notebook.
The selected features were run on different algorithms like logistic, random forest, SVM and Naive Bayes. The best model was selected based on metrics like accuracy, precision and recall and performance.

Model       | Accuracy           | Precision  | Recall
------------- |:-------------:| -----:|:-------
Logistic regression     | 0.72 | 0.74 | 0.85
Random Forest           | 0.76 | 0.80 | 0.82
SVM                     | 0.76 | 0.79 | 0.85
Naive Bayes             | 0.65 | 0.70 | 0.76


 **Random Forest and SVM(Support Vector Machines) have the best result. We chose Ramdomforest since it is faster and will perform better with larger datasets.**
 The parameters of randomforest algorithm was tuned to get the best fit. Details about this are available in the notebook.

 ### 5 Conclusions and recommendations

 **1.We saw that a high percentage of Android users have churned compared to iPhone users. The company might want to look at their Android app to figure out why Android users are not as active as Iphone users.**

**2.The company should look at the number of trips taken in the first 30 days by the customer. If the number of trips average at 3.3 and higher, there is a good chance that this user will be an active user. This feature allows us the company to predict if a customer will churn or not in the future.**

**3.The active users tend to use the luxury car more than inactive users. The company can focus more can luxury car services and see if it improves retention.**

**4.King's landing city has a higher ratio of active users. The company should look at the reasons and figure out if the same active users ratio can be increased in the other 2 cities.**
