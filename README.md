# Linear-regression-model-for-identifying-factors-affecting-car-prices
This project builds a linear model to identify the factors affecting prices of cars for a manufacturer entering the US market.

# Data set
The data set has car prices for 205 cars along with features such as make of the car, engine type, engine location, number of doors etc. for each of the cars.

# Data preprocessing
The data is checked for presence of null values and none are found. Further, all categorical columns are converted to dummy variables. It is found that a variation of spellings is present for different car makes. Therefore, alternative spellings are converted to one standard spelling before proceeding with model building.
## Normalization and Recursive Feature Elimination (RFE)
The data is normalized using a custom min-max scaler. RFE is used to narrow down on relevant features and remove multicollinearity. This preprocessed data is then used for further model building and evaluation

# Model building
Multiple linear regression models are implemented. Before moving on to the next model, the statistical summary of the current linear regression model is studied and features with high p values are dropped from the data set, as well as features with high Variance Inflation Factor (VIF) values are dropped.

# Model evaluation
After iterating over 12 linear regression models as described in the 'Model building' section above, the data set contains five most critical features for predicting the car price. Predictions are made using the final model on the test data and the predicted values are plotted alongside actual values. 

# Conclusion
The following features are found to affect car prices significantly. The names of these factors along with their relative weights in the linear regression model are given below.

drivewheel_rwd            5583.621504
enginetype_rotor        -13368.310936
cylindernumber_four     -10032.909139
cylindernumber_twelve    10336.689064
fuelsystem_2bbl          -2691.303658
