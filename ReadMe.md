# Read me

## Assignment description

The purpose of this assignment is to demonstrate how to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.

As the result should be created one R script that does the following with the original dataset:
1) Merges the training and the test sets to create one data set.
2) Extracts only the measurements on the mean and standard deviation for each measurement.
3) Uses descriptive activity names to name the activities in the data set
4) Appropriately labels the data set with descriptive variable names.
5) From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## Orignal dataset

### License

For the assignment was used the "Human Activity Recognition Using Smartphones" Dataset (version 1.0).

Original data set was crated by:
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Universitа degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws

For more information about dataset contact: activityrecognition@smartlab.ws

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.


### Original dataset description

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

### Use of original dataset data

From the original dataset for the purpose of assignment was used following info:
* A 561-feature vector with time and frequency domain variables. 
* Its activity label. 
* An identifier of the subject who carried out the experiment.

Following information from dataset was not used:
* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
* Triaxial Angular velocity from the gyroscope. 

Above mentioned data included the following data files:
* 'features.txt': List of all features.
* 'activity_labels.txt': Links the class labels with their activity name.
* 'train/X_train.txt': Training set.
* 'train/y_train.txt': Training labels.
* 'test/X_test.txt': Test set.
* 'test/y_test.txt': Test labels.
* 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
* 'test/subject_test.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

## Tidy dataset

### Tidy dataset description

Tidy dataset consists of one file: "tidydataset.txt"
This file contains information about the average value for each variable for each activity and each subject from the transformed orginal data set.

Columns of tidy dataset:
1) "variable" - subset of names of original dataset features selected by the criteria that on them were applied mean() and std() functions and their name contains substring "mean()"/"std()"
2) "activity_name" - name of 6 fctivities listed in the "activity_labels.txt" file in original dataset
3) "subject_id" - id of one of 30 subjects participated in experiment
4) "mean(value)" - avarage value of each variable, each activity and each subject applied to variables with "mean()" substring.


### Script for tidy dataset

Transforming script could be found in the "run_analysis.R" file.
Full comments for the work of the script provided in the CodeBook file.

---

For more information about dataset contact: puborisov@gmail.com

Pavel Borisov. February 2016.