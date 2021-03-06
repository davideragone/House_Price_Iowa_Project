# House_Price_Iowa_Project
Repo for the Regression House Price competition project:

https://www.kaggle.com/c/iowa-house-prices-regression-techniques/data

# Project Overview

* Exploratory Data Analysis, outliers identification and data cleaning.

* Modelling using Random Forest, CatBoost amd XGBoost Regressors.

* Hyperparameters tuning usings RandomizedSearchCV amd  GridSearchCV.

* Test set predictions.

## Code and Resourses used

**Python Version:** 3.8.2

**Packages:** Pandas, Numpy, Matplotlib, Seaborn, SKlearn, XGBoost, CatBoost

## EDA: Exploratory Data Analysis
The EDA made shows how data is distributed and relation between different features. Following few highlights from the graphs dispalyed:

![alt text](https://github.com/davideragone/House_Price_Iowa_Project/blob/main/Pictures/Corr_matrix.png)
![alt text](https://github.com/davideragone/House_Price_Iowa_Project/blob/main/Pictures/First_floor_Sale_price_regplot.png)
![alt text](https://github.com/davideragone/House_Price_Iowa_Project/blob/main/Pictures/Qual_price_scatter.png)



## Data Cleaning
First use the pandas api to clean the Train dataset (df1) as follow:

* Fill missing numerical values with feature median
* Convert Object data into numerical
* Create a binary column for missing data with Boolean values

Then functionize the whole process with a `preprocess_data(df)` function that performs same transformations.

## Model Building 

* Split Data into `train` and `test` data

* Create `fit_and_score(model)` function to instantiate and compare accuracy from different estimators simultaneously.

* 3 different estimators:
Random Forest Classifier
XGBoost Classifier
CatBoost Classifier

* Hyperparameter tuning using RandomizedSearchCV and GridSearchCV for the two best performant classifiers.

## Make predictions
Once evaluated the best model which gives the lowest RSLME, use it to make predictions on test data.
