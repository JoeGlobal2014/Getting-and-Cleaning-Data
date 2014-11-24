Getting and Cleaning Data: Course Project

by Joe Reed



Introduction

This repository contains my work for the course project for the Coursera course "Getting and Cleaning data", part of the Data Science specialization. What follows first are my notes on the original data.

About the raw data

The features (561 of them) are unlabeled and can be found in the x_test.txt. The activity labels are in the y_test.txt file. The test subjects are in the subject_test.txt file. The same holds for the training set.

About the script and the tidy dataset:

I created a script called run_analysis.R which will merge the test and training sets together. Prerequisites for this script:

the UCI HAR Dataset must be extracted and..
the UCI HAR Dataset must be availble in a directory called "UCI HAR Dataset"
This allows the if your working directory contains the folder "UCI HAR Dataset" which in turn has the folders for the data "test" and "train"; the script will run.
Assume that you are in the working directory when you execute the script and the  the UCI HAR Dataset must be availble in the working directory called "UCI HAR Dataset"
it then contains the two folders "train" and "test" which contain the Samsung data
X_train.txt,Y_train.txt,subject_train.txt in the "train" folder and X_test.txt,Y_test.txt,
subject_test.txt in the "test" folder.  Of course we expect the activity_labels.txt to be in the 
UCI HAR Dataset folder.

After merging testing and training, labels are added and only columns that have to do with mean and standard deviation are kept.

Lastly, the script will create a tidy data set containing the means of all the columns per test subject and per activity. This tidy dataset will be written to a tab-delimited file called tidy.txt, which can also be found in this repository. I choose tab delimited becasue their were no specifications not to so I felt I was free to do so.  I did however use the row.names = FALSE addition to the write.table command as instructed.

About the Code Book

The CodeBook.md file explains the transformations performed and the resulting data and variables.
