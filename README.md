# Spark-predict-user-churn
Spark predict customer churned
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Exploratory Data Analyst](#exploratory)
5. [Feature engineer](#feature)
6. [Modelling](#modelling) 
7. [Conclusion](#conclusion) 

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*.
test
## Project Motivation<a name="motivation"></a>

For this project, I was interestested in using Spark data to better understand of the customer churn following the process below:

### Load and clean Dataset
1. Add the columns time, date, month and year to the dataset
2. Remove the user id null
3. extract state from location

This steps will help to perform a deeper analysis in the dataset.
The file related to this course are owned by udacity, so they are not publicly available here.  

### File Descriptions <a name="files"></a>

This dataset is part of skarky, and the data source can be found in udacity.
There are 18 columns in the dataset:

root

 |-- artist: string (nullable = true)
 
 |-- auth: string (nullable = true)
 
 |-- firstName: string (nullable = true)
 
 |-- gender: string (nullable = true)
 
 |-- itemInSession: long (nullable = true)
 
 |-- lastName: string (nullable = true)
 
 |-- length: double (nullable = true)
 
 |-- level: string (nullable = true)
 
 |-- location: string (nullable = true)
 
 |-- method: string (nullable = true)
 
 |-- page: string (nullable = true)
 
 |-- registration: long (nullable = true)
 
 |-- sessionId: long (nullable = true)
 
 |-- song: string (nullable = true)
 
 |-- status: long (nullable = true)
 
 |-- ts: long (nullable = true)
 
 |-- userAgent: string (nullable = true)
 
 |-- userId: string (nullable = true)


### Define churn
An extract column is added to define the churned customers using "Cancelation Confirmation" within the field "page" to define the events. The event could happend for paid or free users.

## Exploratory Data Analyst<a name="exploratory"></a>
Once we have all the columns in place some exploratory data analyst needs to be done to observe the users interactions and behaviors and compare churned users with users that stay.
Aggregate values to calculate the number of users per page or per artics and see the number of sessions per day to check the trends during the period of study.
Page events and level by user churn status (0,1).

## Feature engineer<a name="feature"></a>

add a few functions to calculate the necessary features and create the dataset to be used in machine learning. Also, explore some of the data in the dataset.

## Modelling<a name="modelling"></a>

Split the full dataset into train and test. Using machile learning test some methods and evaluate the accuracy of several models.
1- Logistic regresion

2- RandomForestClassifier

3- GBTClassifier

4- LinearSVC

## Conclusion<a name="conclusion"></a>
after the analysis of the 4 models the Decision Tree Classifier model looks to be the best here
