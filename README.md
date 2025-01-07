# Bike-Sharing-Demand-Prediction-Capstone-Project

## 📖 Introduction

The business problem is to ensure a stable supply of rental bikes in urban cities by predicting the demand for bikes at each hour. By providing a stable supply of rental bikes, the system can enhance mobility comfort for the public and reduce waiting time, leading to greater customer satisfaction.

To address this problem, we need to develop a predictive model that takes into account various factors that may influence demand, such as time of day, seasonality, weather conditions, and holidays. By accurately predicting demand, the bike sharing system operators can ensure that there is an adequate supply of bikes available at all times, which can improve the user experience and increase usage of the bike sharing system. This can have a positive impact on the sustainability of urban transportation, as it can reduce congestion, air pollution, and greenhouse gas emissions.


## 📖 Dataset Information and Preparation

* There are 24 logs(one for each hour of the day) of bike rental data recorded consistently for each day.
* The ‘Date’ attribute has the date of the recording stored as a string. This attribute is converted to
datetime format and features indicating day of the week, weekends, different times of the day and month are collected.
* Features such as hour of the day, day of the week and month are not exclusively continuous. These features are rather cyclic in nature and this
needs to be reflected to capture routines and recurring behaviors in the data we are interested in predicting.
* The physical data describing the weather in the city of Seoul are temperature, humidity, windspeed, visibility, solar radiation, rainfall and snowfall. 
* The dataset contains features such as Weekend and Holiday that might explain sudden fluctuations in
activity. There are 18 holidays in Seoul where one might notice a demand trend varying from a regular workday trend.


## 📖 EDA Observations and findings

* From Exploratory Data Analysis, we found that the bike rentals follow an hourly trend
where it hits the first peak in the morning and the highest peak next, in the evening.
* It was also found that these trends are prominent only during weekdays and working days, leading us to make a safe assumption that office-goers make a notable contribution in bike sharing demand. 
* In addition, seasons were observed to have a notable effect on bike rentals, seeing high traffic during the summers and a significant
low during the winters.


## 📖 Evaluation Metric
The metrics measured for evaluating performance of bike share prediction models are:
  * MSE
  * RMSE
  * MAE
  * R-SQUARED, and
  * Adjusted R-SQUARED

## 📖 ML Models Evaluated

As the data available is collected only over the period of one year, time-series forecasting is not considered. But instead, traditional regressive Machine Learning Models are trained and evaluated
  * Linear Regression 
  * Lasso Regression 
  * Ridge Regression
  * Decision Tree
  * Random Forest
  * XG Boost


The top models are picked to tune hyperparameters in order to further optimize
their results. These models are also stacked and evaluated using Stacking
Ensemble.

## 📖 Results

* Upon evaluation, the Linear models (Linear Regression, Lasso Regression and Ridge Regression)
performed nominally and increased with regularization. This improvement only explained 52.00% of the variance at best.

* Hyperparameter tuning increased the R squared scores of these models to 0.9369, 0.9216 and 0.9093 respectively.

* Upon evaluation, the Stacking Regressor’s( CatBoost, LightGBM and Random Forest) score was 0.938, outperforming all the other models.

## 📖 Conclusions

* The top two models were XGBoost , Random Forest, 

* Their results were further optimized using hyperparameter tuning. 

  ● It was found that the top performing models made predictions based on the weather
and time of the day as high weightage was given to seasons, temperature recorded
and hour of the day.


## 📜 Credits
* Project Done by Vaibhav Mande
* Project Verified by Almabetter


