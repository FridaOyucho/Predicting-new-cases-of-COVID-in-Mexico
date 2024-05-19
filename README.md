# Predicting-new-cases-of-COVID-in-Mexico
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/0c791c29-af23-45ed-8c1d-9e178476f92d)

Author : Frida Oyucho

## Overview
This repository contains the code and documentation for a project focused on utilizing machine learning  models to analyze and predict new cases of covid 19 in Mexico . The dataset used for this project contains information  conditions that clients had when they were tested for COVID in Mexico in 2020.

##Business problem
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/7ae24c26-56e9-4ed4-b49b-c2e9fdc994ba)

This project aims to provide an in-depth analysis of the COVID-19 situation in Mexico and develop a machine learning-based model to predict new cases of the virus. By leveraging historical data on COVID-19 cases, the project seeks to identify trends, patterns, and potential correlations with various factors that may contribute to the spread of the virus. The insights gained from this analysis and the predictive model will help inform public health policies and strategies for better managing and mitigating the impact of the pandemic.

## Data Understanding
The data was extracted from the Government of Mexico's ministry of Health national data repository. The data conatins 10,000 rows with 22 columns. The target variable for modelling is['covid_res']and predictor variables after preprocessing the data areas listed:['sex', 'patient_type','month_name', 'intubed', 'pneumonia', 'pregnancy', 'diabetes', 'copd', 'asthma', 'inmsupr', 'hypertension', 'other_disease', 'cardiovascular', 'obesity', 'renal_chronic', 'tobacco', 'contact_other_covid', 'icu','dead','age_groups']

## Methodology
The data analysis was based on clients tested for COVID clients  between January to December 2020
1. Data preparation was done to align data types, detect and deal with:
   -   missingness
   -   duplicate records
   -   outliers
2. Feature engineering was done to two variable: ‘dead’ , ‘age_groups’ and ‘month_names’

3. Exploratory Data analysis was done on: Univariate, Bi-variate and Multivariates. This was done by:
     -  assesing descriptive statistics of the dataset
    - visualizing outputs in Barcharts, piechart, Histograms and linegrapghs to understand the distribution and correlation of various features.
4. Data Preprocessing was done to prepare the data for modeling(Normalization using Standardscalar & One hot enocoding)

5. Data modelling was done using three models: Logistic Regression, Random Forest & XGboost
  -  Split-Train Test
  -  Normalization
  -  One Hot Encoding(for categorical variables)
  -  Model Evaluation
  -  Visualization of:
      -  Classification Report
      -  Confusion Matrix
      -  ROC Curve

  ## Results
  Univariate Analysis:
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/c4cff40a-fd80-4735-852e-30d0c16fc6cc)

72% of deaths were from clients who tested positive

Bivariate Analysis:
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/ab46c239-e3f2-44b3-a899-8aa2f13e7af7)

Peak positivity rates was in the period of
May 2020.

Multivariate Analysis:
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/75b8be5b-913f-4e47-aedd-8397530ac62c)

Modelling
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/06911313-7cf6-466a-97f7-cbd1a26b8b6d)

Hyperparameter tuning was done using grid search to all the models. The model that performed the best was XGBoost with an AUC of 67%

Feature Importance:
![image](https://github.com/FridaOyucho/Predicting-new-cases-of-COVID-in-Mexico/assets/63707906/1d0265e7-3e2b-48f3-ae9a-a0937d50ac9e)

From the model that performed the best, the top 5 features of importance were:
  1. Patient_type_outpatient
  2. died_0 
  3.  date_symptoms
  4.   copd clients
  5.   cardiovascular clients

##Conclusion
Majority of clients who had covid were from the age of 50-69 years they should be monitored more closely.
55.7% of positive cases were from Males. Males are at high risk of getting infected as compared to females who had an infection rate of 44.3%
From the data, disease which contributed the most to the infection was ‘contact_other_covid’, pneumonia, hypertension,obesity & diabetes
The model that performed the best was XGBoost with tuning from gridsearchCV.

##Recommendations










  
