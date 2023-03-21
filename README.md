
# Data Scientist Nanodegree

## Project : Starbucks-Capstone-Challenge







## Project Motivation

In this project, my aim is to identify which Starbucks customers are likely to complete a promotional offer versus just viewing it. To accomplish this, I will be analyzing a set of simulated data that imitates customer behavior on the Starbucks rewards mobile app. By analyzing this data, we can gain insights into customer behavior and potentially make more informed decisions.

The challenge we face is in identifying which customers to offer our promotions to. We want to ensure that we are only offering promotions to those who are likely to complete them. Offering promotions to customers who are unlikely to complete them is a waste of valuable time and resources. To tackle this challenge, I will first clean the data and conduct exploratory analysis to identify our most valuable customers. Afterward, I will develop a predictive model that takes into account customer age, gender, income, and spending habits to determine the likelihood of a customer completing a promotional offer after viewing it.
## Dataset

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. 

An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that is the challenge to solve with this data set.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product. 


## Data Dictionary

The data is contained in three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)

profile.json - demographic data for each customer

transcript.json - records for transactions, offers received, offers viewed, and offers completed
Here is the schema and explanation of each variable in the files:

## portfolio.json

id (string) - offer id

offer_type (string) - type of offer ie BOGO, discount, informational

difficulty (int) - minimum required spend to complete an offer

reward (int) - reward given for completing an offer

duration (int) - time for offer to be open, in days

channels (list of strings)


## profile.json

age (int) - age of the customer

became_member_on (int) - date when customer created an app account

gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)

id (str) - customer id

income (float) - customer's income


## transcript.json

event (str) - record description (ie transaction, offer received, offer viewed, etc.)

person (str) - customer id

time (int) - time in hours since start of test. The data begins at time t=0

value - (dict of strings) - either an offer id or transaction amount depending on the record

## Installation

Install my-project with npm

```bash
Python versions 3.*.
Python Libraries:
Pandas
matplotlib
seaborn
Scikit-learn
numpy
time


```
    
## Result

In this project, I tried to analyze and make model to predict whether a Starbucks customer will just view the offer or complete it. First I explored the 3 datasets that were provided by looking at things such as missing values, duplciates, datatype and range and joted the changes that needs to be done. Then I did the necessary preprocessing on the data by creating features and converting them into a format that can be merged. All the 3 datasets were then merged to get a master database. Then EDA was performed to check the impact of differnt features on dependent variable. The EDA showed that majority customers are above the age of 40 years. Customers with income more than $70K per year have better completion rate and should be targeted. Female customers also have better completion rate than males and should be targeted. Then I built a classification model with offer viewed vs offer completed as the dependent variable. Various classification techniques such as Decision Tree, SVM, Random forest, Naive Bayes Classifier, Logistic Regression and KNN were tried and the technique that gave a good F1 score and more generalized result (train and test f1 score similar) was chosen - SVM with 0.68 F1 score
## Licensing, Authors, Acknowledgements

 - The data was given by Starbucks and Udacity. Feel free to ask me anything about the code [GitHub](https://github.com/chintandand93/Capstone-project)


