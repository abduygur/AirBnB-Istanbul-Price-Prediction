# AirBnB Istanbul Price Prediction

Here is the medium story about this project: https://abduygur.medium.com/airbnb-hosts-and-where-to-find-them-4c204dfd1138

Outline of the project:

1- Overview of the Dataset

2- Preprocessing

3- Modeling and Evaluation

After some descriptive analysis, predict airbnb listing prices with the 35 attributes using Random Forest Regression and XGB Regression

# Data:

- Data is very messy with 22K Rows and 74 Columns.
- Filled null values with looking for other attributes
- Some of them filled manually looking at the listings URL
- Some of them containing lists with string format (like amenities).
- I created a function for taking lists from the row and insert into the columns
- Some True False columns are string format. Converted them to Boolean Column
- Some Percentage columns are string format. Converted them to Numeric Column
- Price column which is my dependent variable is highly skewed so that transformation with logarithm has been applied


# Modeling

This is the prediction of the numeric value so that i use regression techniques. In the first part i fit the columns which i processed to Random Forest Regression and see the models performance. 

After Residual analysis i dropped some rows because this observations effects my model to decreasing R2 Score
Then try Random Forest Regression and XGB regression with Test Set R2 and MSE Score

# Result

I got nearly 0.60 R2 score and 0.28 MSE (In logarithmic price scale) 

