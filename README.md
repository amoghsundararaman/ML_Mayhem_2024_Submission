## Competition: ML Mayhem

## Written by: Amogh Sundararaman (106120012)

## Task Flow:
    - Data Acquision (Unzipping the Data File provided)
    - Setting up imports and initializations
    - Preliminary Data Exploration (loading data, checking for data sanity, missing value checks, Box Plot analysis, pair plot analysis)
    - Correlation based analysis (Hypothesis Testing, Correlation Heatmap)
    - Splitting Data and Standardization (Standard Scaling, Test-Train Split, Hold out data to check performance on unseen data)
    - Model Building and Iteration (Model Selection, Tuning, Evaluation, Building)
    - Feature Importance and Contribution Analysis (Getting feature importances)
    - Testing Predictions on Test Data
    - Reverse Scaling Process for better context
    - Performance Evaluation  (MSE, MAE, R2)
    - Finalizing Model Builds (pickling for storage)
    - Statistical Regressor Model (OLS, building, testing, evaluation, rescaling, finalizing)
    - Final Model Summary (Summarizing Model Performance

## Detailed Description
    
This is a systematic approach to solving the problem statement which is based in regression. 
I first performed a high-level sieve of the data to check that everything in the data is as per the problem statement specifications
Then I performed a preliminary data exploration to check distribution, missing values and sanity checks. 
Once satisfied with data hygiene, I moved on to correlation analysis where I tested the statisitcal significance of each feature in its correlation with the target variable. 
All p values indicated high levels of statistical significance and hence feature elimination wasn't neccessary
Then a correlation heatmap was plotted to further validate the extents of these correlations. 
Once the splitting of data and standard scaling was done to prevent skewness, the Next stage was model building. 
A pycaret iteration was performed to identify the best model (Spoiler Alert: XGBRegressor)

This model was then built out seperately and then tuned using the best parameters obtained from PyCaret. 

Once satisfied with performance, inverse scaling was performed to get context during model summary. 

As an additional step, a statistical OLS based model was also built, tested for performance and stored once a comparable level of performance was achieved. 

All models were pickled out for future usability and the final model performance summary was documented. 

Unscaled performances mean the MSE, MAE, R2 on raw data scale. 
Scaled performances mean the MSE, MAE, R2 on the StandardScalar scale.
Note: The Standard Scaler has also been pickled out for recreating results in future if desired. 
