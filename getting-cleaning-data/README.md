## Getting and Cleaning Data -  Course Project
Week 3 - project submission

### Overview
Project object is to generate tidy data set in text file for future analysis purpose. 

### Project Summary

Create R script called "run_analysis.R" , does the following :
1. Download data set from  above provided path in to working directory
2. Load and read data from the activity , training 
3. Merges the training and the test sets to create one data set.
4. Extracts only the measurements on the mean and standard deviation for each measurement. 
5. Uses descriptive activity names to name the activities in the data set
6. Appropriately labels the data set with descriptive activity names. 
7. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 


### Result is in tidyData.txt

## Code Book - Additional information

### Data Source  
Reference : The UCI Machine Learning Repository
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

#### Note : Set correct working directory before execute 

### Attribute Information
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

### Section 1. Merge the training and the test sets to create one data set.
After setting the source directory for the files, read into tables the data located in
- features.txt
- activity_labels.txt
- subject_train.txt
- x_train.txt
- y_train.txt
- subject_test.txt
- x_test.txt
- y_test.txt

Assign column names and merge to create one data set.

## Section 2. Extract only the measurements on the mean and standard deviation for each measurement. 
Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others.
Subset this data to keep only the necessary columns.

## Section 3. Use descriptive activity names to name the activities in the data set
Merge data subset with the activityType table to cinlude the descriptive activity names

## Section 4. Appropriately label the data set with descriptive activity names.
Use gsub function for pattern replacement to clean up the data labels.

## Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject. 
Per the project instructions, we need to produce only a data set with the average of each veriable for each activity and subject