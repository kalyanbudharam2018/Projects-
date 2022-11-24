# Prediction of Customer Audiobooks Project Overview 

### Problem 

You are given data from an Audiobook App. Logically, it relates to the audio versions of books ONLY. Each customer in the database has made a purchase at least once, that's why he/she is in the database. We want to create a machine learning algorithm based on our available data that can predict if a customer will buy again from the Audiobook company.

The task is simple: create a machine learning algorithm, which is able to predict if a customer will buy again. 

This is a classification problem with two classes: won't buy and will buy, represented by 0s and 1s. 


Summary:

* Collected ‘AudioBook App' dataset from Kaggle, then Pre-processed, Balanced, Normalized & saved in npz files with Python & its libraries (Numpy, Sci-kit Learn).
* Built a Deep Learning Model (with layers as 10, 50, 2), applied early-stopping mechanism, Adam optimizer and obtained 91.07% Model Accuracy with Numpy & TensorFlow.


## Dataset:
The datasets are taken from Kaggle (size_14084 rows × 12 columns).

## Balance the dataset
After collecting the data, I needed to balance the data so that it was usable for further processing. I made balancing the data by removing redundant records.

## Standardizing the dataset
* Used sklearn functionality to take advantage of its preprocessing capabilities for standardizing the inputs.

## Shuffle the dataset
* When the data was collected it was actually arranged by date
* Shuffle the indices of the data, so the data is not arranged in any way when I feed it.
* Used the shuffled indices to shuffle the inputs and targets.

## Split the dataset into train, validation, and test and finally saved the three datasets in *.npz for further modelling.


## Analytics and commercial application
 
In this task, I saved the prepared files for further application. I loaded the saved npz files and built deep learning model (Neural networks) with TensorFlow having following details.
 
 * input_size = 10
 * output_size = 2
 * hidden_layer_size = 50
 * activation functions- relu and softmax
 * optimizer - adam
 * batch size and max_epochs - 100
 * Applied an early stopping mechanism wit patience=2
 
 ## Model Performance
 After the model tested and obtained accuracy- 91.07% with test loss- 24% 





## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** numpy, TensorFlow

**Kaggle Website for Data source**
https://www.kaggle.com/
