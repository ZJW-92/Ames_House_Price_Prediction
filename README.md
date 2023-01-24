# ***Case study: Feature Engineering-- Ames house price prediction***
<p align="left"><img src="img/description.png" width="40%"></p>

## ***1 Problem statement*** 

_In this case study, you will prepare Ames Housing Dataset in a csv file in a way that it is suitable for a ML algorithm. 
You will achieve this by first exploring the data and performing feature transformations on provided dataset of house price prediction ML problem. You are required to train a ML model by using linear regression, ridge regression and lasso regression 
for predicting house prices._

## ***2 Steps***
- _2.1 Load data set_
- _2.2 Exploratory Data Analysis (EDA)_
- 1. Histograms

<img src="img/histograms.png" width="70%">

- 2. Heatmap

<img src="img/heatmap.png" width="50%">


- 3. Scatterplots 

![scatter-view](img/scatterplot.png)


- 4. Scatter matrix 

![scatter_matrix-view](img/scatter_matrix.png)

-  5. Correlation between other features and 'SalePrice'

<img src="img/sale_price_correlation.png" width="20%">

***The target 'SalePrice' variable is highly correlated with features such as OverallQual, GrLivArea, GarageCars, GarageArea and TotalBsmtSF among others.***

- _2.3 Process dataset for ML_

Steps:

- 1. Handle missing values 
- 2. Fill nulls for 'LotFrontage' with median value calculated after grouping by 'Neighborhood'
- 3. Fill nulls for 'GarageYrBlt','MasVnrArea' with 0
- 4. Apply log-transform on target feature 'SalePrice'
- 5. One-hot encoding

## ***3 Train Linear Regression***

Split dataset in training set (X_train, y_train) and test set (X_test, y_test)

## ***4 Evaluate Linear Regression model***
***R^2 score on trainig set: 0.94609, MSE score on trainig set: 0.00808***

***R^2 score on test set: 0.89136, MSE score on test set: 0.01472***

![linear_regression-view](img/linear_regression.png)

## ***5 Model refinement with Ridge regression and Lasso regression***
***Ridge regression (alpha=0.05): R^2 score on training set: 0.94598, R^2 score on test set:  0.89410***

***Lasso regression (alpha= 0.0001): R^2 score on trainig set:  0.94169, R^2 score on test set:  0.90843***


## ***6 Conslusion***: 
_**6.1 In practice, ridge regression is usually the first choice between two models.**_

_**6.2 However, if you have a large amount of features and expect only a few of them to be important, Lasso might be a better choice.**_

|_R^2 score_ |_Linear Regression_ |_Ridge Regression_ |_Lasso Regression_
| --- | --- | --- | --- |
|_training set_| _0.94609_ | _0.94598_ | _0.94169_ |
|_test set_| _0.89136_ |_0.89410_ |_0.90843_ |


