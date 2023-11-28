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

STEP 4: Optimization
•	LR 2 – Increased the max_iter from 200 to 1000 – 86% accuracy.
•	LR 3 - Scaled the variables using Standard scalar – 86% accuracy.
•	LR 4 – Feature selection and scaled variables – 86% accuracy. 

Conclusion:


