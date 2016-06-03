# Introduction

The `run_analysis.R` script performs the 5 steps described required in the in the course project's definition.

* First, both the training and test data is merged using the R `rbind()` function. Additinally, the files files having the same number of columns and reference the same entities are included.
* Only those columns with the "mean" and "standard deviation" measuremewnts are extracted from the whole dataset. Once these columns are extracted, they are given the correct labels and found in the `features.txt` file.
* The activity data is addressed with values 1:6, the activity names and IDs are taken from `activity_labels.txt` and are inserted into the dataset.
* Note that those columns with vague column names are specified for more accuracy.
* Finally a new dataset is generated with all the average measurements for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called `averages_data.txt`, and is pushed to this GitHub repository.

# Variables

* `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` contains the data from the downloaded files.
* `x_data`, `y_data` and `subject_data` merge the previous datasets for further analysis.
* `features` contains the correct names for the `x_data` dataset, which are applied to the column names stored in `mean_and_std_features`, a numeric vector used to extract the desired data.
* A similar approach is taken with activity names through the `activities` variable.
* `all_data` merges `x_data`, `y_data` and `subject_data` in a big dataset.
* Finally, `averages_data` contains the relevant averages which will be later stored in a `.txt` file. `ddply()` from the plyr package is used to apply `colMeans()`.