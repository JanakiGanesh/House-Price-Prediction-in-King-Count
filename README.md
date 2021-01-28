# House Price Prediction in King County
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/high-angle-view-of-suburban-houses-ip-galanternik-du.jpg)

## Introduction

This project focuses on investigating the house sales in King County area. It involves building a regression model to predict the house price. This project helps in finding the various criteria that stimulates the housing price .


## Business Problem

Homeowners approaches the real estate agency for help in order to buy /sell their homes. The business problem that we could focus on for the real estate agency is the need to provide advice to homeowners about home renovations that might increase the estimated value of their homes, and by what amount. In this project we are providing the prediction data to the real estate agency for homeowners who wants to buy homes. It focus on the factors that increases the house price that might be negotiated while purchasing new homes.

## The Data

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this project repo. The description of the column names can be found in `column_names.md` in the same folder. 

## Approach

In this project we are following OSEMN data science workflow. It contains:

* Obtain (Generate data)
* Scrub (extracting columns,handling missing values)
* Explore (understanding data and create visualization)
* Model (building regression model)
* Interpret (communicating results)

## Analysis

We explored our King County House Data and created different regression model to meet regression assumptions and to predict the housw price.

### Model 1 :
First created a baseline model with few variables .\
Train RMSE: 236467.87482500693
Test RMSE: 242081.30788978518
Train R2: 0.5833310228392444
Test R2: 0.5728609089897383\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model1.png)

Our model didn't meet the regression assumptions and the RMSE value was high with low R2 value.

### Model 2 :

Selected variables which are linear and built a new model.\
Train RMSE: 238114.36314309336\
Test RMSE: 243234.25014980324\
Train R2: 0.5775084222015455\
Test R2: 0.568782614551135\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model2.png)

This model didn't improve well. Hence built MOdel 3 
### Model 3 :
Tried log transformation for the target and the response variable\
Train RMSE: 0.3417654821862211\
Test RMSE: 0.34131400565596115\
Train R2: 0.5800369077132734\
Test R2: 0.575725504061078\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model3.png)
Our model 3 improved well on RMSE value but the R squared value improved but let us try improving the model with better R squared value
### Model 4 :

Checking for the muliticollinearity to improve our model

Train RMSE: 0.3513999392706709\
Test RMSE: 0.35286466512965453\
Train R2: 0.5560254312136382\
Test R2: 0.5465232245990275\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model4.png)
The model R2 square value is reduced by small amount
 ### Model 5 :
There were many bathrooms and hence selected only upto 4 bathroom houses and converted them to catergorical variable to improve our model.\
 Train RMSE: 0.33420217863454416\
Test RMSE: 0.34145241899517415\
Train R2: 0.5668054800701774\
Test R2: 0.5687840686619469\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model5.png)

There is no big difference in our R2 and RMSE value and hence I am removing the categorical terms.
 ### Model 6 :

In our dataset we have 'yr_built', 'yr_renovated' and 'grade' column. Checked for interactions between them and applied in our model.\
 Train RMSE: 0.3132980216188752\
Test RMSE: 0.3193145255976609\
Train R2: 0.647085067318093\
Test R2: 0.6286563030309209\
![alt text](https://github.com/JanakiGanesh/House-Price-Prediction-in-King-Count/blob/main/images/Model6.png)

The new model looks better in terms of both R2 value and RMSE value.


## Recommendations

If you are looking for housing that won't make your bank account fragile, then go for the housing with minimal bathroom so that you could share them and it's advisable to shrink on squarefootage that would make our house purchase a very cost effective one.

## Conclusions

Our model RMSE for the train and test set are similar which indicates that our model will perform well on different data. Hence our model can be used as a predictor for the Real Estate Agents to buy house or to analyze the various criteria that stimulates the housing price .

