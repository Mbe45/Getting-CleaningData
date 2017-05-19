==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws

Due credit to the above authors:
I have edited the original readme file 
Mbecho Techago Emmanuel
19/05/2017
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'

- 'run_analysis.R script'

- 'A codebook explaining all the variables and how the raw data was collected and process to a tidy data. codebook.txt

For more information about this dataset contact: activityrecognition@smartlab.ws

###################################################################################################################################

1)the raw data was downloaded from the course- getting and cleaning data offer by John Hopskin university through coursera.
2)the train data set was read into R usung the read.table function in R
3)the subject_id was read into R using read.table fucntion in R
4)the activity lebels for the train dataset was read into R using read.table
5)subject id with the train label set(y_train) was bind using cbind function (column bind)
6)the features, which contains the names of the variables in trainset was read into R using read.table
7)the features names was then assign to the train dataset.
8)the combind subject id and y_label dataset was then column bind to the train data set
9) the first two variables names was change to subject id and activity.
10)producedure 2-9 was followed for the test dataset.
11)the train and test data was row bind using rbind function to form mergedata set
12)the measurements on the mean and standard deviation for each measurement was extracted
using regular expression function grep()

13) giving descriptive activity names to the activity variable by passing
the variables into a factor function and assigning the levels meaningful names
like 1 = "WALKING",2 ="WALKING_UPSTAIRS",3="WALKING_DOWNSTAIRS", 4="SITTING", 5 ="STANDING", 6 ="LAYING"

14) the tidy_data was then created using dplyr package, by grouping it into activity and subject id to look 
for the mean of each activity for each individual during each window period for all the variables.

15) the software use for this analysis was R language for statistical computing, version 3.3.1 (2016-06-21)



License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
