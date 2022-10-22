
# Absenteeism during work time: Project Overview 

* Created a tool that predicts absenteeism at a company during work time which will helpful to regulate working activity and also explore whethera person presenting certain characteristics is expected to be away from work at some point time or not.

* I have collected data from Kaggle in csv file, Pre-processed (Cleaning/ Analysis) data with Python & SQL, finally saved pre-processed data in csv file.
* Applied Feature Engineering, Logistic Regression (ML) with sklearn, obtained 73% accuracy, saved model using pickle
* Model deployed through absenteeism module and Analysed the Predicted Outputs in Tableau.

## Dataset:
This dataset is taken from Kaggle which is famous for it employment service and data has following features:
*	ID
*	Reason for Absence
*	Date
*	Transportation Expense
*	Distance to Work 
*	Age
*	Daily Work Load Average
*	Body Mass Index
*	Education
*	Children 
*	Pets
*	Absenteeism Time in Hours



## Data Cleaning
After collecting the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

*	Dropping unnecessary ID column from dataset
*	Created dummies for Reason for Absence column, later grouped and added into 4 category columns
*	Reordered the 4 reason columns like original dataset order
*	Converted date string data type to datetime datatype 
*	Made a new columns for Month value and Day of the week
*	And made many more changes which can be viewed in the pre-processed data csv

## Exploratory Data Analysis (EDA)
Performed EDA on the cleaned data and got various insights, relationships, etc, few of them are as below.

* There are total 700 rows and 14 columns after pre-processed data
* There are total 28 unique type of values presents in the Reason for absence column
* 4 types of values presents in the Education column, highest being the value 1


## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.   

I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.   

I tried three different models:
*	**Multiple Linear Regression** – Baseline for the model
*	**Lasso Regression** – Because of the sparse data from the many categorical variables, I thought a normalized regression like lasso would be effective.
*	**Random Forest** – Again, with the sparsity associated with the data, I thought that this would be a good fit. 

## Model performance
The Random Forest model far outperformed the other approaches on the test and validation sets. 
*	**Random Forest** : MAE = 11.22
*	**Linear Regression**: MAE = 18.86
*	**Ridge Regression**: MAE = 19.67

## Productionization 
In this step, I built a flask API endpoint that was hosted on a local webserver by following along with the TDS tutorial in the reference section above. The API endpoint takes in a request with a list of values from a job listing and returns an estimated salary. 


## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, selenium, flask, json, pickle  
**For Web Framework Requirements:**  ```pip install -r requirements.txt```  
**Scraper Github:** https://github.com/arapfaik/scraping-glassdoor-selenium  
**Scraper Article:** https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905  
**Flask Productionization:** https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2



