# Advertisement Recommendation Model In R

# Research Questions

Create a prediction model that more accurately predicts whether a user will click an Ad or not.

# Problem Statement

A Kenyan entrepreneur has created an online cryptography course and would want to advertise it on her blog. She currently targets audiences originating from various countries. In the past, she ran ads to advertise a related course on the same blog and collected data in the process which would be used for anlaysis.

# Context
We have 1000 rows

We have the following columns:

  'Daily.Time.Spent.on.Site'
  
  'Age'
  
  'Area.Income'
  
  'Daily.Internet.Usage'
  
  'Ad.Topic.Line'
  
  'City'
  
  'Male'
  
  'Country'
  
  'Timestamp'
  
  'Clicked.on.Ad'

# Steps Followed

  1.Loading Data
  
  Using tidyverse library
  
  2.Data Exploration/Cleaning
  
  Renamed the columns
  
  There were no missing values and duplicates
  
  The few outliers that were avilable i dint remove them so that we can identify the reasons as to why they exist
  
  
  3.Model Training
  
  I used KNeighbours Classifier to fit the model
  
  4.Model Prediction
  
  using the split data to make predictions
  
  5.Metrics of success

  Confusionmatrix
  
       ypred
y_test  0  1
     0 98  2
     1 11 89
  
  Crosstable
  
               | ypred 
      y_test |         0 |         1 | Row Total | 
-------------|-----------|-----------|-----------|
           0 |        98 |         2 |       100 | 
             |     0.980 |     0.020 |     0.500 | 
             |     0.899 |     0.022 |           | 
             |     0.490 |     0.010 |           | 
-------------|-----------|-----------|-----------|
           1 |        11 |        89 |       100 | 
             |     0.110 |     0.890 |     0.500 | 
             |     0.101 |     0.978 |           | 
             |     0.055 |     0.445 |           | 
-------------|-----------|-----------|-----------|
Column Total |       109 |        91 |       200 | 
             |     0.545 |     0.455 |           | 
-------------|-----------|-----------|-----------|

  Accuracy
  
  93.5%
