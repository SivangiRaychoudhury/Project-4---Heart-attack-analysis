Project 4
Diagnosing Heart attacks using Machine Learning

Team members: Caroline Foshee, Evan Woodard, Jamee Jones, Sivangi Raychoudhury

Introduction:
A heart attack (Cardiovascular disease) occurs when the flow of blood to the heart muscle suddenly becomes blocked. According to WHO statistics, 17.9 million people are dying from heart attack each year. The medical study says that human lifestyle is the main reason behind this heart problem. 
This dataset contains some medical information of patients which tells whether the chance of that person getting a heart attack is less or more. Data analysis of heart attack cases provides valuable insights into predicting and preventing heart attacks by examining patients' clinical characteristics and risk factors. Analyzing large datasets can reveal significant patterns and identify risk factors, contributing to more effective guidance of healthcare interventions.
In the notebook, Heart_Attack_Analysis.ipynb, we will conduct an analysis on influential factors related to heart attacks. Subsequently, we will make predictions on the probability of individuals experiencing a heart attack, using different Machine Learning models and comparing their outputs to get the best model. 
The dataset we worked on was found from Kaggel.com and the link to the page is: https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset/data

STEP 1: Importing required libraries and Data cleaning
•	Load the csv and convert into Pandas DataFrame
•	Get the brief summary of the df
•	Describe the df
•	Check for the nulls and duplicates

STEP 2: Exploratory Data Analysis (EDA)
•	Check for the unique value counts for all the variables 
•	Divided the variables into 2 groups: Numeric and Categoric
•	Numeric: With high unique values (age, trtbps, chol, thalachh, oldpeak)
•	Categoric: With few unique values (sex, cp, fbs, restecg, exng, slp, caa, thall, output)
•	Performed the univariate analysis of numeric variables and the analysis is described after each plot. 
•	Bi-variate analysis of numeric variables and the output variable(target). This gave some idea about which variables are correlated with the output variable. 
•	Then the univariate analysis of categoric variable was done and the detailed analysis output was described below the plots generated. 
•	Bi-variate analysis of categorical variables and the output variable was done. 

STEP 3: Different Machine Learning Models
We used 4 models for comparision: 
•	Logistic Regression
•	Decision Tree
•	Random Forest
•	Neural Network

For all these models we split the data into training and testing data. Used the necessary dependencies and produced the accuracy and precision along with the confusion matrix. The accuracy scores for the different models are the following:
•	Logistic Regression - 87%
•	Decision Tree – 83%
•	Random Forest – 87%
•	Neural Network – 80%

To determine which model best identifies heart attacks, we ran four models initially. Both the logistic regression and random forest models gave the highest accuracy of 87%. We chose logistic regression for further optimization for a variety of reasons:
1.Logistic regression models are easier to interpret.
2.They are less computationally intensive than random forest models so they are easier to train and optimize.
3.They are less prone to overfitting, and overfitting may be a significant issue when trying to determine which symptoms are most related to heart attack incidence.

STEP 4: Optimization
•	LR 2 – Increased the max_iter from 200 to 1000 – 86% accuracy.
•	LR 3 - Scaled the variables using Standard scalar – 86% accuracy.
•	LR 4 – Feature selection and scaled variables – 86% accuracy. 

Conclusion:
To create the best logistic regression model, we changed a variety of variables:
1. Max iterations: When we increased this number to 1000, the accuracy decreased, and one additional patient was misclassified compared to Logistic Regression #1.
2. Scaled data: When we used this model with scaled data, the accuracy decreased, and one additional patient was misclassified compared to Logistic Regression #1.
3. Feature selection & scaled: When we used this model with scaled data and feature selection, the accuracy decreased, and one additional patient was misclassified compared to Logistic Regression #1.

Therefore, our first logistic regression is the best model in terms of accuracy. As demonstrated in the chart "Coefficients of Logistic Regression Model", sex was the most significant determinant of heart attack incidence, with males having more heart attacks than females. Type of chest pain was the second most significant variable, followed by incidence of exercise induced angina, average ST depression, number of major vessels colored by fluoroscopy, and thalassemia score. The following variables are not significant: age, resting blood pressure, cholesterol levels, fasting blood sugar, electrocardiogram results, and slope of the peak exercise ST segment.

