# Housing Case Study
Using Ridge and Lasso regression to identify the driving factors behind house prices in the Australian market.

## Table of Contents
*# Lending Club Case Study

## Table of Contents
* [General Info](#general-information)
* [Dataset](#dataset)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
The purpose of this project was to identify the driving factors behind house prices in the Australian market.

Ridge and Lasso regression models were constructed for the prediction of house prices.  Regularization was applied to reduce overfitting and increase model generalizability.

The requirements were to identify:
* Which variables are significant in predicting the price of a house
* How well those variables describe the price of a house

## Dataset
The analyzed dataset was supplied as part of the UpGrad AI&ML programme.  The dataset can be found [here](https://ml-course3-upgrad.s3.amazonaws.com/Assignment_+Advanced+Regression/train.csv).

Summary of the dataset:
- Number records: 1460
- Number of columns: 81

## Methodology
The dataset was prepared for processing by replacing 'NA' values with values that would be interpreted correctly.  Categorical variables that have very few distinctive values were removed from the dataset.  Records that have outliers in the target variable have also been removed.  Derived variables have been created to capture elapsed time.  Dummy categorical variables were introduced and the dataset was normalized.  A total number of 163 predictor variables were used in the final model.

Ridge and Lasso regression models were trained against 75% of the records in the supplied dataset.  Regularization was applied to reduce model variance.  A Lasso regression model with alpha=0.0004 for regularization was selected as the final model.  The model selected 75 predictor variables out of 163.  The model was evaluated against the remaining 25% of the records in the supplied dataset.

## Conclusions
The following strong driving factors behind housing prices have been identified (top 20):

| Predictor | Coefficient |
|--|--|
| BsmtFullBath | 0.357785 |
| OverallCond | 0.233686|
| GarageArea | 0.086154 |
| Neighborhood OldTown | 0.080115 |
| Neighborhood Timber | 0.066244 |
| Neighborhood NridgHt |  0.057923|
| Exterior CemntBd | 0.050917 |
| ExterCond | 0.049402 |
| TotRmsAbvGrd | 0.041497|
| BsmtFinSF1 | 0.041328 |
| BsmtCond | 0.040899
| Functional | 0.039718
| Neighborhood Edwards | 0.039649
| EnclosedPorch | 0.032692
| BldgType 2fmCon | 0.031646
| MasVnrArea | 0.031629
| BsmtHalfBath | 0.031535
| OpenPorchSF | 0.030701
| Exterior VinylSd| -0.028481

## Technologies Used
The following Python libraries were utilized:
- Pandas
- Numpy
- Seaborn
- Matplotlib
- Sklearn
- Scipy
- Statsmodels

## Contact
Created by @gertagenbag