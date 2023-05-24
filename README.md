![pexels-abhishek-saini-3026026](/Images/pexels-abhishek-saini-3026026.jpg)
### Introduction
 * SyriaTel is trying to understand the churn level of its customers and what should be done to maximize profits.

### 1.Business Understanding
 * problem statement
This project aims to help and guide SyriaTel on predicting the patterns that leads to customers churn. By doing so, SyriaTel will be able to manimize the losses incured due to the customers that don't still around for long. At the end, with the predictions SyriaTel will be able to make better decisions based on the final recomendations derived from the in depth Data analysis. 
 
##### Specific objectives
Is there a relationship between people with the least total charges and churn status?
Does the customer service calls affect churn status?
What is the relationship between account length have with the churn status?
Does the area code affect the churn status?
The effects of total minutes with to the churn status.
International total usage compared to the churn status.

##### Success metrics

- This project will focus on the accuracy as the success metric

### 2. Data Understanding
 * state - the state the user lives in
account length - the number of days the user has this account
 * area code - the code of the area the user lives in
 * phone number - the phone number of the user
 * international plan - true if the user has the international plan, otherwise false
 * voice mail plan - true if the user has the voice mail plan, otherwise false
 * number vmail messages - the number of voice mail messages the user has sent
 * total day minutes - total number of minutes the user has been in calls during the day
 * total day calls - total number of calls the user has done during the day
 * total day charge - total amount of money the user was charged by the Telecom company for calls during the day
 * total eve minutes - total number of minutes the user has been in calls during the evening
 * total eve calls - total number of calls the user has done during the evening
 * total night minutes - total number of minutes the user has been in calls during the night
 * total night calls - total number of calls the user has done during the night
 * total night charge - total amount of money the user was charged by the Telecom company for calls during the night
* total intl minutes - total number of minutes the user has been in international calls
 * total intl calls - total number of international calls the user has done
 * total intl charge - total amount of money the user was charged by the Telecom company for international calls
 * customer service calls - number of customer service calls the user has done
 * churn - true(encoded as 1) if the user terminated the contract, otherwise false(encoded as 0)
 
##### Data Source

 * https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset
 
##### Data description

- The data had 21 columns and 3333 rows

### 3. Data preparation 
#####  Data cleaning
 - load data
 - check and deal with missing values
 - Check for duplicates
 - Dealing with extraneous values
 - Check for outliers
 - Describing data using summary statistics 
#####  Explanatory Data Analysis
 - The churn status was 85.5 % stayed while 14.5 stopped beign customers.
 - The charges had normal distribution
 - It was evident that the clients who did't have the international plan continued being customers as compared to those had the plan. This meant that having the international plan did't stop the customers from leaving.
 - The customers who had a voice mail plan were less compared to those who didn't purchase the plan. 2000 customers which is 60% of the data didn't have the voice mail plan and they decided to stay.
 - The area code determined the total number of customers that wanted to transact with SyriaTel. The area code between 300-400 had more subscriptions and more customers were willing to continue transacting and a very small number less that 10% of the customers that did churn.
 - Customer loyalty is witnessed as those customers who stayedwere those that had been using SyriaTel for long compared to the most current ones.
 ##### Correlation
 - To check if the data has columns that correlate with each other which was positive in this data. 
 
### 4. Modelling
##### a) Total Customer Charge, Minutes and calls
 - To avoid overfitting of the models, there was need to combine how much each customer was getting charge, how many minutes they were consuming and the number of calls they made from morning to night.
##### b) One Hot Encoding
 To change the categorical columns for easier modelling.
##### c) Data Splitting
 Performing train test split to split the data into training and test data.
##### d) Models
  Logistic Regression Model
 -  The Logistic Regression Model was the data's vanilla model which performed with an accuracy_score of 85.90 %. This is considered to have performed well.
 
  * K Nearest Neighbour Model
 - The model performed well with an accuracy 89.65% which was an improvement from the vanilla model.
 
  * Decision Tree Model
  
 - We pick this as the best performing model as it had the best accuracy score of 90.10%. At this point, each model performed was getting better. 
 
  * Random Forest Model
 - Used grid_search to help pick the best performing model and introduced a penalty; cross valiation of 5 to get the best performing. The accuracy was 96.55% which was okay but was almost overfitting. 
 
### 6. Conclusion

 - The churn status was affected by the total customer charges, intenational plan, customer service calls, area, voice mail plan and account length.
 - The data was also biased area wise which was not as sufficient though a very important variable to analyse. 
 - The model confusion matrix performed well for predictions and the actual churn status. 
### 7. Recommendation
 - SyriaTel should consider improving the area coverage to attract more customers and to reduce the churn levels.
 - The international plan maybe an expensive idea as it doesn't win the customer loyalty. The plan should be reconsidered to minimize losses and for the company to attract even more customers.
 - The company should come up with a plan where those that spend most in a day are either rewarded or their calling rates are reduced at a certain point of the day. This is because, it was evident the more the customers spent in a day, the higher the chances of churning ehich is a loss for the company.
  -  The voice mail plan doesn't should be reconsidered either by evaluating the customers culture of maybe preferring phone calls over voice mail or by reducing its charging rates to attract more of both new and current suctomers.