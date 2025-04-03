# Predicting-Academic-Perfomance

## Project Objective 

Our goal is to develop a predictive model that estimates student academic performance (GPA) based on lifestyle and study-related factors. The goal is to uncover meaningful patterns in student behavior and provide data-driven insights into academic success. We are going to create a regression model that takes survey data as input and estimates academic performance. Our end product would be a well-evaluated model, clear visualizations, and an explanation of our results of which features matter the most.

## Our Motivation 

Students often struggle to find the right balance between studying, sleep, and extracurriculars. By analyzing patterns across students, we can offer data-driven insights into which lifestyle choices are most predictive of academic achievement, potentially guiding students to make more informed decisions.

## Week-by-Week Overview

Week 1-2 → start putting together survey and getting responses

Week 2 → survey review and data exploration, understand the dataset and perform EDA with plots and summaries

Week 3 → data cleaning and prep, clean data ready for modeling

Week 4 → build baseline regression model, initial accuracy and prediction plots

Week 5 → feature importance analysis, ranked features and insight discussion

Week 6 → final visualizations and polish, ready to share visuals and write up

# Let's Start the Project 

## Getting the Data 

For this project, you will use a dataset collected from college student surveys, which would contain lifestyle and study-related factors that could affect GPA. The first step would be to come up with questions for the survey. You could use 'Qualtrics' or 'Google Forms' for this. A few factors for example could be something like study hours, sleep hours, extracurricular hours, stress level, or time management. I think we should try and aim to get 150-200 responses if possible? Once we have our responses, we can convert them to a dataset and familiarize ourselves with the data.

## Libraries 

For this project we will be using these libraries: 'pandas' for loading and cleaning data, 'numpy' for numerical operations, 'matplotlib' for plotting graphs, 'seaborn' for visualizations, and scikit-learn (sklearn) - for machine learning models. 

## Understanding the Data 



## Techniques We Will Use

We will use the sklearn library for this. 

Linear Regression (baseline model)

Linear Regression is a simple model that draws a straight-line relationship between inputs and the outcome (GPA). This technique is really good for getting started and setting a benchmark. *Hint* We can use 'sklearn.linear_model' which contains 'LinearRegression'.

Decision Tree Regression

This is a model that splits the data into branches based on feature values. It captures non-linear relationships better than linear regression. *Hint* We can use 'sklearn.tree' which contains 'DecisionTreeRegressor'.

You might also need to use 'sklearn.model_selection' which contains the 'train_test_split'. The purpose of this is to split the dataset into 2 parts, where one trains the model, and one tests how well it performs on the data. You can split your features (X) and lables (y) into 'X_train', 'X_test', 'y_train', and 'y_test'. You can also use 'sklearn.preprocessing' which contains 'StandardScaler'. This helps standardize your features byr emoving the mean and scaling to unit variance. You would use this to fit in on your training data, and then transform both training and test sets the same way. You can also use 'sklearn.metrics' which contains 'r2_score', and 'mean_squared_error'. 'r2_score' tells you how well your model explains the variability in the data. Basically, the closer it would be to 1 means teh better it is. A score of 0 would mean the model is no better than just predicting the average GPA. The MSE (mean squared error) measures how far off your predictions are from the true values, but it squares the errors, so that the big mistakes are looked at more. You would interpret this as the lower the MSE, the better. You can use this to compare how each regression model performs. 

## Feature Importance Analysis

After building our models, we will look at which features had the most weight in Linear Regression and which features were used most frequently in Decision Trees. For example, we could see whether study hours or sleep have a bigger impact on GPA. In Linear Regression you would check the coefficients of each feature. The bigger values (positive or negative) would mean that the feature had more influence. In Decision Trees, the features that appear higher up in the tree or are used more frequently in splits are more important. 

## Visualizations 

Lets create three visualizations. I have provided a guided setup for making each visualization. 

1) Actual vs. Predicted GPA Plot - scatter plot that compares real GPAs vs. what the model predicted which would help us assess how accurate the model is. 
```
# After training your model, use it to predict on the test data
# y_pred = model.predict(X_test)

# Create a scatter plot comparing actual vs. predicted GPA
# Use a plotting library (like matplotlib or seaborn)

# X-axis: y_test (actual GPA)
# Y-axis: y_pred (predicted GPA)

# Add a reference line showing perfect predictions (y = x)
# Helps you visually see if predictions are above or below the actual values
```
2) Heatmaps - shows the correlations between all variables and it helps us spot patterns early in the process.
```
# Make sure the dataset is numeric (drop or encode categoricals if needed)
# Use the .corr() function to compute a correlation matrix
# corr_matrix = df.corr()

# Use a heatmap tool (like seaborn.heatmap)
# Set annot=True if you want the correlation values to show in each square
```  

4) Feature Importance Chart - Bar plot that shows which features the model relied on the most.
Linear Regression:
```
# Get the .coef_ values from your linear model
# These are the feature weights

# Pair each coefficient with the corresponding feature name
# (you can get the feature names from your original dataframe or feature set)

# Take absolute values of coefficients if you want to rank by strength

# Sort the values before plotting
``` 
Decision Tree:
```
# Use the .feature_importances_ attribute from the tree model

# Combine these with your feature names

# Plot a bar chart with the top features
``` 
## Deliverables 

By the end of this project we should have a clean, well-documented dataset, a regression model that predicts GPA, feature importance findings, and visualizations comparing actual vs predicted GPA. We can include our findings at the end as well. For example we can answer these questions: What survey features do we expect to be most predictive? How should we handle categorical data like time-management? Should we try multiple models or focus on one? What would success look like for our model?
