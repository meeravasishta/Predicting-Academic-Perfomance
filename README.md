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

## Understanding the Data 

For this project, you will use a dataset collected from college student surveys, which would contain lifestyle and study-related factors that could affect GPA. The first step would be to come up with questions for the survey. A few factors for example could be something like study hours, sleep hours, extracurricular hours, stress level, or time management. I think we should try and aim to get 150-200 responses if possible? Once we have our responses, we can convert them to a dataset and familiarize ourselves with the data.

## Techniques We Will Use

Linear Regression (baseline model)

Linear Regression is a simple model that draws a straight-line relationship between inputs and the outcome (GPA). This technique is really good for getting started and setting a benchmark.
Decision Tree Regression

This is a model that splits the data into branches based on feature values. It captures non-linear relationships better than linear regression.
Random Forest Regression

This is basically an ensemble of many decision trees working together.

## Feature Importance Analysis

After building our models, we will look at which features had the most weight in Linear Regression and which features were used most frequently in Decision Trees. For example, we could see whether study hours or sleep have a bigger impact on GPA.

## Visualizations 

Lets create three visualizations

1) Actual vs. Predicted GPA Plot - scatter plot that compares real GPAs vs. what the model predicted which would help us assess how accurate the model is.

2) Heatmaps - shows the correlations between all variables and it helps us spot patterns early in the process.

3) Feature Importance Chart - Bar plot that shows which features the model relied on the most.

## Deliverables 

By the end of this project we should have a clean, well-documented dataset, a regression model that predicts GPA, feature importance findings, and visualizations comparing actual vs predicted GPA. We can include our findings at the end as well. For example we can answer these questions: What survey features do we expect to be most predictive? How should we handle categorical data like time-management? Should we try multiple models or focus on one? What would success look like for our model?
