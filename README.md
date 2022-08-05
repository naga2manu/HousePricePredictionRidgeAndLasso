Housing Price Prediction using Ridge and Lasso Regression

**Problem Statemenet:**

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

The company wants to know:

	Which variables are significant in predicting the price of a house, and How well those variables describe the price of a house.

	Also, determine the optimal value of lambda for ridge and lasso regression.

**Business Goal**
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

**Approach Taken:**
- Reading and Understanding the Data
- Basic Data Cleanup
  - Missing value check and imputation using Business Logic.
  - Statistical imputation of missing values
- Exploratory Data Analysis:
  - Performed Univariate and Bi-variate analysis on identified variables.
  - Correlation heatmap
- Data Preparation for model building:
  - Performed log transformation of target variable.
  - Train-Test Split.
  - Encoding categorical (nominal) features
  - Performed Scaling of numerical features
- Model Building:
  - Ridge Regression model with GridSearchCV to find optimal value of alpha.
  - Lasso Regression model with GridSearchCV to find optimal value of alpha.
  - Evaluate both the model on training and test dataset.


**Observations:**
- Ridge and Lasso both the models have almost same test and train accuracy. So it can be said that there is no overfitting.
- Lasso and Ridge both have similar r2 score, RSS, MSE ad RMSE on test dataset. But Lasso has eliminated 78 features and final number of features in Lasso Regression model is 45. Where Ridge has all 123 features. So, our Lasso model is simpler than Ridge with having similar r2 score and MAE.
    - Ridge Regression model on test dataset: r2 score= 0.858400, RSS= 10.204889, MSE= 0.023299, RMSE= 0.152640
    - Lasso Regression model on test dataset: r2 score= 0.852958, RSS= 10.597121, MSE=0.024194, RMSE= 0.155545
     
- Considering above points we can choose our Lasso Regression model as our final model.


