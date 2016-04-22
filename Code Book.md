Code Book
Introduction
The script run_analysis.R performs the 5 steps described in the course project's definition.
•  First, all the similar data is merged using the rbind() function. By similar, we address those files having the same number of columns and referring to the same entities.
•  Then, only those columns with the mean and standard deviation measures are taken from the whole dataset. After extracting these columns, they are given the correct names, taken from features.txt.
•	As activity data is addressed with values 1:6, we take the activity names and IDs from activity_labels.txt and they are substituted in the dataset.
•	On the whole dataset, those columns with vague column names are corrected.
•	Finally, we generate a new dataset with all the average measures for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called tidy_avg_data.txt, and uploaded to this repository.
Variables
•	x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
•	x_data, y_data and subject_data merge the previous datasets to further analysis.
•	features contains the correct names for the x_data dataset, which are applied to the column names stored in meanstd_features, a numeric vector used to extract the desired data.
•	A similar approach is taken with activity names through the activities variable.
•	all_data merges x_data, y_data and subject_data in a big dataset.
•	Finally, tidy_average_data contains the relevant averages which will be later stored in a .txt file. The melt() function from the reshape2 package is used to create the average of each activity and each subject.
Identifiers
•	subject - The ID of the test subject
•	activity - The type of activity performed when the corresponding measurements were taken
Measurements
1.	tBodyAccMeanX
2.	tBodyAccMeanY
3.	tBodyAccMeanZ
4.	tBodyAccStdX
5.	tBodyAccStdY
6.	tBodyAccStdZ
7.	tGravityAccMeanX
8.	tGravityAccMeanY
9.	tGravityAccMeanZ
10.	tGravityAccStdX
11.	tGravityAccStdY
12.	tGravityAccStdZ
13.	tBodyAccJerkMeanX
14.	tBodyAccJerkMeanY
15.	tBodyAccJerkMeanZ
16.	tBodyAccJerkStdX
17.	tBodyAccJerkStdY
18.	tBodyAccJerkStdZ
19.	tBodyGyroMeanX
20.	tBodyGyroMeanY
21.	tBodyGyroMeanZ
22.	tBodyGyroStdX
23.	tBodyGyroStdY
24.	tBodyGyroStdZ
25.	tBodyGyroJerkMeanX
26.	tBodyGyroJerkMeanY
27.	tBodyGyroJerkMeanZ
28.	tBodyGyroJerkStdX
29.	tBodyGyroJerkStdY
30.	tBodyGyroJerkStdZ
31.	tBodyAccMagMean
32.	tBodyAccMagStd
33.	tGravityAccMagMean
34.	tGravityAccMagStd
35.	tBodyAccJerkMagMean
36.	tBodyAccJerkMagStd
37.	tBodyGyroMagMean
38.	tBodyGyroMagStd
39.	tBodyGyroJerkMagMean
40.	tBodyGyroJerkMagStd
41.	fBodyAccMeanX
42.	fBodyAccMeanY
43.	fBodyAccMeanZ
44.	fBodyAccStdX
45.	fBodyAccStdY
46.	fBodyAccStdZ
47.	fBodyAccJerkMeanX
48.	fBodyAccJerkMeanY
49.	fBodyAccJerkMeanZ
50.	fBodyAccJerkStdX
51.	fBodyAccJerkStdY
52.	fBodyAccJerkStdZ
53.	fBodyGyroMeanX
54.	fBodyGyroMeanY
55.	fBodyGyroMeanZ
56.	fBodyGyroStdX
57.	fBodyGyroStdY
58.	fBodyGyroStdZ
59.	fBodyAccMagMean
60.	fBodyAccMagStd
61.	fBodyBodyAccJerkMagMean
62.	fBodyBodyAccJerkMagStd
63.	fBodyBodyGyroMagMean
64.	fBodyBodyGyroMagStd
65.	fBodyBodyGyroJerkMagMean
66.	fBodyBodyGyroJerkMagStd
Activity Labels
•	WALKING (value 1): subject was walking during the test
•	WALKING_UPSTAIRS (value 2): subject was walking up a staircase during the test
•	WALKING_DOWNSTAIRS (value 3): subject was walking down a staircase during the test
•	SITTING (value 4): subject was sitting during the test
•	STANDING (value 5): subject was standing during the test
•	LAYING (value 6): subject was laying down during the test
