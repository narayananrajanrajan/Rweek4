Code Book

This code book includes information about the source data, the transformations performed after collecting the data and some information about the variables of the resulting data sets.

Study Design

The source data was collected from the UCI Machine Learning Repository to complete an assignment for a Coursera course named Getting and Cleaning Data instructed by Jeff Leek. The assignment involved working with the data set and producing tidy data representation of the source data. Below is a list of the operations done to achieve the outputs.

1. Downloaded the data set

2. Unzipped the data set into my chosen working directory

3. Loaded test and training data sets into data frames


4. Loaded source variable names for test and training data sets


5. Loaded activity labels


6. Combined test and training data frames using rbind


7. Paired down the data frames to only include the mean and standard deviation variables


8. Replaced activity IDs with the activity labels for readability


9. Combined the data frames to produce one data frame containing the subjects, measurements and activities


10. Produced "sensor_data_mean_std" with the combined data frame as the first expected output


11. Created another data set using the data.table library to easily group the tidy data by subject and activity


12. Then applied the mean and standard deviation calculations across the groups


13. Produced "sensor_avg_by_act_sub.txt" as the second expected output


Variables:-
The set of variables that were estimated from these signals are:
Variable:
1. mean(): Mean value

2.std(): Standard deviation

3.mad(): Median absolute deviation

4.max(): Largest value in array

5.min(): Smallest value in array

6.sma(): Signal magnitude area

7.energy(): Energy measure. Sum of the squares divided by the number of values.

8.iqr(): Interquartile range

9.entropy(): Signal entropy

10.arCoeff(): Autoregression coefficients with Burg order equal to 4

11.correlation(): Correlation coefficient between two signals

12.maxInds(): Index of the frequency component with largest magnitude

13.meanFreq(): Weighted average of the frequency components to obtain a mean frequency

14.skewness(): Skewness of the frequency domain signal

15.kurtosis(): Kurtosis of the frequency domain signal

16.bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.

17.angle(): Angle between some vectors.

Name	Time domain	Frequency domain
1. Body Acceleration	TimeDomain.BodyAcceleration.XYZ	FrequencyDomain.BodyAcceleration.XYZ

2. Gravity Acceleration	TimeDomain.GravityAcceleration.XYZ	

3. Body Acceleration Jerk	TimeDomain.BodyAccelerationJerk.XYZ	FrequencyDomain.BodyAccelerationJerk.XYZ

4. Body Angular Speed	TimeDomain.BodyAngularSpeed.XYZ	FrequencyDomain.BodyAngularSpeed.XYZ

5. Body Angular Acceleration	TimeDomain.BodyAngularAcceleration.XYZ	

6. Body Acceleration Magnitude	TimeDomain.BodyAccelerationMagnitude	FrequencyDomain.BodyAccelerationMagnitude

7. Gravity Acceleration Magnitude	TimeDomain.GravityAccelerationMagnitude	

8. Body Acceleration Jerk Magnitude	TimeDomain.BodyAccelerationJerkMagnitude	FrequencyDomain.BodyAccelerationJerkMagnitude

9. Body Angular Speed Magnitude	TimeDomain.BodyAngularSpeedMagnitude	FrequencyDomain.BodyAngularSpeedMagnitude

10. Body Angular Acceleration Magnitude	TimeDomain.BodyAngularAccelerationMagnitude	FrequencyDomain.BodyAngularAccelerationMagnitude

11. For variables derived from mean and standard deviation estimation, the previous labels are augmented with the terms "Mean" or "StandardDeviation".

12. The data set is written to the file sensor_avg_by_act_sub.txt.
