# CodeBook
Description: This code book describes variables, data and work performed to cleanup the data

## Assumptions
We are assuming that data is unzipped into the working directory, so run_analysis.R runs from the same directory (commented out for Github)

## Variables
* activity_labels, feature_names (for feature names and activites)
* X_test, y_test to load and process X_test and y_test data
* extract_features - to extract measurments on mean and SD for each measurment

test_data train_data - test and training data
data - merge test and train data
tidy_data - holds value after we apply mean function to dataset using dcast function

## Transformations
For each of the training and test datasets we read in X values, take a subset of columns representing only mean and SD
We also associate additional columns to represent activity ID and subject ID
We merge training and test data sets to create one data set
Melt dataset by specifying actitity ID, subject, activity label
Apply mean function to dataset using dcast f-n
And write result in tidy_data

