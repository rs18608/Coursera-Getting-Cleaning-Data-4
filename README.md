Getting and Cleaning Data - Course Project
==========================================

This repository contains the R code and documentation files for the Data Science's track course "Getting and Cleaning data", available in coursera.

The dataset being used is: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## Files

The `run_analysis.R` assumes that the data required is found in the ./UCI HAR Dataset folder extracted from the original compressed file `getdata-projectfiles-UCI HAR Dataset.zip`.

`CodeBook.md` describes the variables and data, along with data transformation as performed by the `run_analysis.R` script and calls to 3rd party libraries to clean and organize the data.

`run_analysis.R` contains all the code that performs the 5 steps described by the assignment. 

The resulting output mentioned in the 5th step is called `averages_data.txt`, and is in this repository.