# getting_and_cleaning_data_PROJECT
Project for the Coursera course Getting and Cleaning Data

Files: 

(a) run_analysis.R
It contains the script used to complet the assignment, wich is divided in the same 5 parts that it is in the Coursera website:
- section 1: the original training and test data is read and it is merged using the command rbind() to create data.frames that contain all the rows from both the test and the train datasets. the new data.frames "X_all" and "y_all" are created, each one containing the data for the datasets X and y respectively.
- section 2: each column of the new dataset created in section 1 is assigned its feature name using the "features.txt" file and the features wich names contain the substring "mean()" or "std()" are extracted (note that other possible substrings like "meanFreq()" have not been included on purpose). A new data.frame, called "X_mean_std" is created containing only the extracted features
- secton 3: the names of the activities are obtained from the file "activity_labels.txt" and are assigned to each of the factor numerical values of the y variable, already containing both training and test data in the "y_all" data.rame
- section 4: already completed in section 2
- - section 5: the split() function is used to split the data in the two levels that are generated by all the possible combinations of "subjects" and "y" using the function "interaction()". Then, the mean is applied by columns using the functions "colMeans()" and, after setting the names of the columns, the variables that contain the means and the standard deviations are extracted using the results of section 2. Finally, the dataset is saved in a .txt file using the function "write.table()". 

(b) CodeBook.md  Contains information of the variables used in the project. It can be used as a reference.

(c) "features_info.txt" Contains information about each feature.

(d) README.md  It is this document.
