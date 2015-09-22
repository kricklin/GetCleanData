# run_analysis.R Codebook
k. ricklin  
Sept. 21, 2015  

##Background
This codebook provides overview for the file **analysis_output.txt** that is created by the **run_analysis.r** script included in the "GetCleanData" repository.

##Data Processing
For an overview of the original HUARS data set and the script  used to create the **analysis_output.txt** file, please see the [README](https://github.com/kricklin/GetCleanData) included with the "GetCleanData" repository.

###analysis_output.r Notes

####Dimensions
180 observations/rows of 82 variables/columns

####Data Summary
- Each row represents a collection of all mean and standard deviation motion measurements assocated with a specific activity for a single voluntter as captured by smartphone technology. 30 volunteers participated. 6 activities were measured for each volunteer.
- With the exception of the subject_id, partition, and activity columns, each column represents the average value for a specific measurement.
 
####Variable Name Guide:
+ "f_" = "frequency"
+ "t_" = "time"
+ "_gyro" = "gyroscope"
+ "_accel" = "accelerometer"
+ "_std" = "standard deviation"

####Variable List:

OLD VARIABLE NAMES                    
 [1] "subject_id"                     
 [2] "partition"                      
 [3] "activity"                       
 [4] "tBodyAcc-mean()-X"              
 [5] "tBodyAcc-mean()-Y"              
 [6] "tBodyAcc-mean()-Z"              
 [7] "tGravityAcc-mean()-X"           
 [8] "tGravityAcc-mean()-Y"           
 [9] "tGravityAcc-mean()-Z"           
[10] "tBodyAccJerk-mean()-X"          
[11] "tBodyAccJerk-mean()-Y"          
[12] "tBodyAccJerk-mean()-Z"          
[13] "tBodyGyro-mean()-X"             
[14] "tBodyGyro-mean()-Y"             
[15] "tBodyGyro-mean()-Z"             
[16] "tBodyGyroJerk-mean()-X"         
[17] "tBodyGyroJerk-mean()-Y"         
[18] "tBodyGyroJerk-mean()-Z"         
[19] "tBodyAccMag-mean()"             
[20] "tGravityAccMag-mean()"          
[21] "tBodyAccJerkMag-mean()"         
[22] "tBodyGyroMag-mean()"            
[23] "tBodyGyroJerkMag-mean()"        
[24] "fBodyAcc-mean()-X"              
[25] "fBodyAcc-mean()-Y"              
[26] "fBodyAcc-mean()-Z"              
[27] "fBodyAcc-meanFreq()-X"          
[28] "fBodyAcc-meanFreq()-Y"          
[29] "fBodyAcc-meanFreq()-Z"          
[30] "fBodyAccJerk-mean()-X"          
[31] "fBodyAccJerk-mean()-Y"          
[32] "fBodyAccJerk-mean()-Z"          
[33] "fBodyAccJerk-meanFreq()-X"      
[34] "fBodyAccJerk-meanFreq()-Y"      
[35] "fBodyAccJerk-meanFreq()-Z"      
[36] "fBodyGyro-mean()-X"             
[37] "fBodyGyro-mean()-Y"             
[38] "fBodyGyro-mean()-Z"             
[39] "fBodyGyro-meanFreq()-X"         
[40] "fBodyGyro-meanFreq()-Y"         
[41] "fBodyGyro-meanFreq()-Z"         
[42] "fBodyAccMag-mean()"             
[43] "fBodyAccMag-meanFreq()"         
[44] "fBodyBodyAccJerkMag-mean()"     
[45] "fBodyBodyAccJerkMag-meanFreq()" 
[46] "fBodyBodyGyroMag-mean()"        
[47] "fBodyBodyGyroMag-meanFreq()"    
[48] "fBodyBodyGyroJerkMag-mean()"    
[49] "fBodyBodyGyroJerkMag-meanFreq()"
[50] "tBodyAcc-std()-X"               
[51] "tBodyAcc-std()-Y"               
[52] "tBodyAcc-std()-Z"               
[53] "tGravityAcc-std()-X"            
[54] "tGravityAcc-std()-Y"            
[55] "tGravityAcc-std()-Z"            
[56] "tBodyAccJerk-std()-X"           
[57] "tBodyAccJerk-std()-Y"           
[58] "tBodyAccJerk-std()-Z"           
[59] "tBodyGyro-std()-X"              
[60] "tBodyGyro-std()-Y"              
[61] "tBodyGyro-std()-Z"              
[62] "tBodyGyroJerk-std()-X"          
[63] "tBodyGyroJerk-std()-Y"          
[64] "tBodyGyroJerk-std()-Z"          
[65] "tBodyAccMag-std()"              
[66] "tGravityAccMag-std()"           
[67] "tBodyAccJerkMag-std()"          
[68] "tBodyGyroMag-std()"             
[69] "tBodyGyroJerkMag-std()"         
[70] "fBodyAcc-std()-X"               
[71] "fBodyAcc-std()-Y"               
[72] "fBodyAcc-std()-Z"               
[73] "fBodyAccJerk-std()-X"           
[74] "fBodyAccJerk-std()-Y"           
[75] "fBodyAccJerk-std()-Z"           
[76] "fBodyGyro-std()-X"              
[77] "fBodyGyro-std()-Y"              
[78] "fBodyGyro-std()-Z"              
[79] "fBodyAccMag-std()"              
[80] "fBodyBodyAccJerkMag-std()"      
[81] "fBodyBodyGyroMag-std()"         
[82] "fBodyBodyGyroJerkMag-std()" 


New Variable Names
 
 1. "subject_id"                    
 2. "partition" w/ 2 levels:
+  "TESTING"
+  "TRAINING"
 3. "activity" w/ 6 levels:
+  "WALKING"
+  "WALKING_UPSTAIRS"
+  "WALKING_DOWNSTAIRS"
+  "SITTING"
+  "STANDING"
+  "LAYING"
 4. "t_body_accel_mean_x"           
 5. "t_body_accel_mean_y"           
 6. "t_body_accel_mean_z"           
 7. "t_gravity_accel_mean_x"        
 8. "t_gravity_accel_mean_y"        
 9. "t_gravity_accel_mean_z"        
10. "t_body_accel_jerk_mean_x"      
11. "t_body_accel_jerk_mean_y"      
12. "t_body_accel_jerk_mean_z"      
13. "t_body_gyro_mean_x"            
14. "t_body_gyro_mean_y"            
15. "t_body_gyro_mean_z"            
16. "t_body_gyro_jerk_mean_x"       
17. "t_body_gyro_jerk_mean_y"       
18. "t_body_gyro_jerk_mean_z"       
19. "t_body_accel_mag_mean"         
20. "t_gravity_accel_mag_mean"      
21. "t_body_accel_jerk_mag_mean"    
22. "t_body_gyro_mag_mean"          
23. "t_body_gyro_jerk_mag_mean"     
24. "f_body_accel_mean_x"           
25. "f_body_accel_mean_y"           
26. "f_body_accel_mean_z"           
27. "f_body_accel_meanfreq_x"       
28. "f_body_accel_meanfreq_y"       
29. "f_body_accel_meanfreq_z"       
30. "f_body_accel_jerk_mean_x"      
31. "f_body_accel_jerk_mean_y"      
32. "f_body_accel_jerk_mean_z"      
33. "f_body_accel_jerk_meanfreq_x"  
34. "f_body_accel_jerk_meanfreq_y"  
35. "f_body_accel_jerk_meanfreq_z"  
36. "f_body_gyro_mean_x"            
37. "f_body_gyro_mean_y"            
38. "f_body_gyro_mean_z"            
39. "f_body_gyro_meanfreq_x"        
40. "f_body_gyro_meanfreq_y"        
41. "f_body_gyro_meanfreq_z"        
42. "f_body_accel_mag_mean"         
43. "f_body_accel_mag_meanfreq"     
44. "f_body_accel_jerk_mag_mean"    
45. "f_body_accel_jerk_mag_meanfreq"
46. "f_body_gyro_mag_mean"          
47. "f_body_gyro_mag_meanfreq"      
48. "f_body_gyro_jerk_mag_mean"     
49. "f_body_gyro_jerk_mag_meanfreq" 
50. "t_body_accel_std_x"            
51. "t_body_accel_std_y"            
52. "t_body_accel_std_z"            
53. "t_gravity_accel_std_x"         
54. "t_gravity_accel_std_y"         
55. "t_gravity_accel_std_z"         
56. "t_body_accel_jerk_std_x"       
57. "t_body_accel_jerk_std_y"       
58. "t_body_accel_jerk_std_z"       
59. "t_body_gyro_std_x"             
60. "t_body_gyro_std_y"             
61. "t_body_gyro_std_z"             
62. "t_body_gyro_jerk_std_x"        
63. "t_body_gyro_jerk_std_y"        
64. "t_body_gyro_jerk_std_z"        
65. "t_body_accel_mag_std"          
66. "t_gravity_accel_mag_std"       
67. "t_body_accel_jerk_mag_std"     
68. "t_body_gyro_mag_std"           
69. "t_body_gyro_jerk_mag_std"      
70. "f_body_accel_std_x"            
71. "f_body_accel_std_y"            
72. "f_body_accel_std_z"            
73. "f_body_accel_jerk_std_x"       
74. "f_body_accel_jerk_std_y"       
75. "f_body_accel_jerk_std_z"       
76. "f_body_gyro_std_x"             
77. "f_body_gyro_std_y"             
78. "f_body_gyro_std_z"             
79. "f_body_accel_mag_std"          
80. "f_body_accel_jerk_mag_std"     
81. "f_body_gyro_mag_std"           
82. "f_body_gyro_jerk_mag_std" 

###Variable Notes
####"subject_id"
Integer - a value ranging from 1 - 30 that identifies each participant.

####"partition"
Factor - an identifier tying a subject to the "TRAINING" or "TESTING" group. 

####"activity"
Factor - identifies one of six activity measurments:
- "WALKING"
- "WALKING_UPSTAIRS"
- "WALKING_DOWNSTAIRS"
- "SITTING"
- "STANDING"
- "LAYING"

Some information on the variable including:
 - Class of the variable
 - Unique values/levels of the variable
 - Unit of measurement (if no unit of measurement list this as well)
 - In case names follow some schema, describe how entries were constructed (for example time-body-gyroscope-z has 4 levels of descriptors. Describe these 4 levels). 

(you can easily use Rcode for this, just load the dataset and provide the information directly form the tidy data file)

####Notes on variable 1:
If available, some additional notes on the variable not covered elsewehere. If no notes are present leave this section out.

##Original HUARS Data Set License
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
