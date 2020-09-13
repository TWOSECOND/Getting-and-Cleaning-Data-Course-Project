File with R code "run_analysis.R" performs the 5 following steps (in accordance assigned task of course work):

1.Download the dataset
Dataset downloaded and extracted under the folder called UCI HAR Dataset

2.Assign each data to variables
incuding features, activities, X_train,X_train,Sub_train,X-test,Y_test,Sub_test, using read.table function

3.Merges the training and the test sets to create one data set
X  is created by merging X_train and X_test using rbind() function
Y  is created by merging Y_train and Y_test using rbind() function
Subject is created by merging Subject_train and Subject_test using rbind() function
Merged_Data  is created by merging Subject, Y and X using cbind() function

4.Extracts only the measurements on the mean and standard deviation for each measurement
TidyData is created by subsetting Merged_Data, selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement

5.Uses descriptive activity names to name the activities in the data set
Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of the activities variable

6.Appropriately labels the data set with descriptive variable names
code column in TidyData renamed into activities
All Acc in column’s name replaced by Accelerometer
All Gyro in column’s name replaced by Gyroscope
All BodyBody in column’s name replaced by Body
All Mag in column’s name replaced by Magnitude
All start with character f in column’s name replaced by Frequency
All start with character t in column’s name replaced by Time

7.From the data set in step 6, creates a tidy data set with the average of each variable for each activity and each subject
FinalData is created by sumarizing TidyData taking the means of each variable for each activity and each subject, after groupped by subject and activity.
Export FinalData into FinalData.txt file.
