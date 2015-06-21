
##Code Book
For the Human Activity Recognition Using Smartphones tidy dataset `MergedAvg` created by the **run_analysis.R** script.

---

**I. Raw data files**

Data files employed to create `MergedAvg` available from the unzipped raw dataset folder 'UCI HAR Dataset'.

* **Training** set 
    * 'train/X_train.txt': measurements
    * 'train/y_train.txt': activity labels
    * 'train/subject_train.txt': subject identifier 
* **Test** set 
    * 'test/X_test.txt': measurements
    * 'test/y_test.txt': activity labels
    * 'test/subject_test.txt': subject identifier 
* **Features/Variables**
    * 'features.txt': list of all features estimated from the measured signals
* **Activities**
    * 'activity_labels.txt': links activity labels to activity names
    
In addition, files 'README.txt' and 'features_info.txt' were used to infer infer information about the raw dataset measurements, files structure, and variables. 

---
  
**II. Notes on summaries and nomenclature**

* **Summaries**
    * Variables [3:68]: are averaged, as mean values, for each subject and each activity.
* **Nomenclature**
    * "body" designates the volunteer person physical body. 
    * "FFT"  designates the Fast Fourier Transform.
    * "X (or Y,Z) direction" designates the X axial direction.
   
---    
  
**III. Variables units**

* Variables [1:2]: categorical 
* Variables [3:68]: normalized and bounded within [-1,1]
   
---    
  
  
**VI. Variables dictionnary**  
  
  
1. **Subject**

          Identifier assigned to the volunteer person who performed the experiment
          Type: numeric
          Range: 1..30

2. **Activity**

          Daily-living activity performed by the person
          Type: character
          Categories: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING 
              
3. **tBodyAcc.mean...X**

          Mean value of the body acceleration signal in the X direction
          Type: numeric
       
4. **tBodyAcc.mean...Y**

          Mean value of the body acceleration signal in the Y direction
          Type: numeric

5. **tBodyAcc.mean...Z**

          Mean value of the body acceleration signal in the Z direction
          Type: numeric

6. **tGravityAcc.mean...X**

          Mean value of the gravity force acceleration signal in the X direction
          Type: numeric

7. **tGravityAcc.mean...Y**

          Mean value of the gravity force acceleration signal in the Y direction
          Type: numeric

8. **tGravityAcc.mean...Z**

          Mean value of the gravity force acceleration signal in the Z direction
          Type: numeric


9.	**tBodyAccJerk.mean...X**

          Mean value of the body Jerk signal, as obtained from the acceleration, in the X direction
          Type: numeric


10.	**tBodyAccJerk.mean...Y**

          Mean value of the body Jerk signal, as obtained from the acceleration, in the Y direction
          Type: numeric
          
11.	**tBodyAccJerk.mean...Z**

          Mean value of the body Jerk signal, as obtained from the acceleration, in the Z direction
          Type: numeric


12.	**tBodyGyro.mean...X**

          Mean value of the body angular velocity in the X direction
          Type: numeric

13.	**tBodyGyro.mean...Y**

          Mean value of the body angular velocity in the Y direction
          Type: numeric
          
14.	**tBodyGyro.mean...Z**

          Mean value of the body angular velocity in the Z direction
          Type: numeric

15.	**tBodyGyroJerk.mean...X**

          Mean value of the body Jerk signal, as obtained from the angular velocity, in the X direction
          Type: numeric
          
16.	**tBodyGyroJerk.mean...Y**

          Mean value of the body Jerk signal, as obtained from the angular velocity, in the Y direction
          Type: numeric

17.	**tBodyGyroJerk.mean...Z**

          Mean value of the body Jerk signal, as obtained from the angular velocity, in the Z direction
          Type: numeric

18.	**tBodyAccMag.mean..**

          Mean value of the magnitude of the body acceleration signal 
          Type: numeric

19.	**tGravityAccMag.mean..**

          Mean value of the magnitude of the gravity force acceleration signal 
          Type: numeric


20.	**tBodyAccJerkMag.mean..**

          Mean value of the magnitude of the body Jerk signal, as obtained from the acceleration 
          Type: numeric


21.	**tBodyGyroMag.mean..**

          Mean value of the magnitude of the body angular velocity
          Type: numeric

22.	**tBodyGyroJerkMag.mean..**

          Mean value of the magnitude of the body Jerk signal, as obtained from the angular velocity 
          Type: numeric
          
23.	**fBodyAcc.mean...X**

          Mean value of the FFT of the body acceleration signal in the X direction
          Type: numeric

24.	**fBodyAcc.mean...Y**

          Mean value of the FFT of the body acceleration signal in the Y direction
          Type: numeric
          
25.	**fBodyAcc.mean...Z**

          Mean value of the FFT of the body acceleration signal in the Z direction
          Type: numeric

26.	**fBodyAccJerk.mean...X**

          Mean value of the FFT of the body Jerk signal, as obtained from the acceleration, in the X direction
          Type: numeric

27.	**fBodyAccJerk.mean...Y**

          Mean value of the FFT of the body Jerk signal, as obtained from the acceleration, in the Y direction
          Type: numeric
          
28.	**fBodyAccJerk.mean...Z**

          Mean value of the FFT of the body Jerk signal, as obtained from the acceleration, in the Z direction
          Type: numeric

29.	**fBodyGyro.mean...X**

          Mean value of the FFT of the body angular velocity in the X direction
          Type: numeric
          
30.	**fBodyGyro.mean...Y**

          Mean value of the FFT of the body angular velocity in the Y direction
          Type: numeric
          
31.	**fBodyGyro.mean...Z**

          Mean value of the FFT of the body angular velocity in the Z direction
          Type: numeric

32.	**fBodyAccMag.mean..**

          Mean value of the magnitude of the FFT of the body acceleration signal 
          Type: numeric
          
33.	**fBodyAccJerkMag.mean..**

          Mean value of the magnitude of the FFT of the body Jerk signal, as obtained from the acceleration 
          Type: numeric
          
34.	**fBodyGyroMag.mean..**

          Mean value of the magnitude of the FFT of the body angular velocity
          Type: numeric

35.	**fBodyGyroJerkMag.mean..**

          Mean value of the magnitude of the FFT of the body Jerk signal, as obtained from the angular velocity 
          Type: numeric


36.	**tBodyAcc.std...X**

          Standard deviation of the body acceleration signal in the X direction
          Type: numeric

37.	**tBodyAcc.std...Y**

          Standard deviation of the body acceleration signal in the Y direction
          Type: numeric
          
38.	**tBodyAcc.std...Z**

          Standard deviation of the body acceleration signal in the Z direction
          Type: numeric

39.	**tGravityAcc.std...X**

          Standard deviation of the gravity force acceleration signal in the X direction
          Type: numeric
          
40.	**tGravityAcc.std...Y**

          Standard deviation of the gravity force acceleration signal in the Y direction
          Type: numeric
          
41.	**tGravityAcc.std...Z**

          Standard deviation of the gravity force acceleration signal in the Z direction
          Type: numeric

42.	**tBodyAccJerk.std...X**

          Standard deviation of the body Jerk signal, as obtained from the acceleration, in the X direction
          Type: numeric
          
43.	**tBodyAccJerk.std...Y**

          Standard deviation of the body Jerk signal, as obtained from the acceleration, in the Y direction   
          Type: numeric

44.	**tBodyAccJerk.std...Z**

          Standard deviation of the body Jerk signal, as obtained from the acceleration, in the Z direction
          Type: numeric

45.	**tBodyGyro.std...X**

          Standard deviation of the body angular velocity in the X direction
          Type: numeric

46.	**tBodyGyro.std...Y**

          Standard deviation of the body angular velocity in the Y direction
          Type: numeric
          
47.	**tBodyGyro.std...Z**

          Standard deviation of the body angular velocity in the Z direction
          Type: numeric

48.	**tBodyGyroJerk.std...X**

          Standard deviation of the body Jerk signal, as obtained from the angular velocity, in the X direction
          Type: numeric
          
49.	**tBodyGyroJerk.std...Y**

          Standard deviation of the body Jerk signal, as obtained from the angular velocity, in the Y direction
          Type: numeric
          
50.	**tBodyGyroJerk.std...Z**

          Standard deviation of the body Jerk signal, as obtained from the angular velocity, in the Z direction
          Type: numeric

51.	**tBodyAccMag.std..**

          Standard deviation of the magnitude of the body acceleration signal 
          Type: numeric

52.	**tGravityAccMag.std..**

          Standard deviation of the magnitude of the gravity force acceleration signal 
          Type: numeric
          
53.	**tBodyAccJerkMag.std..**

          Standard deviation of the magnitude of the body Jerk signal, as obtained from the acceleration 
          Type: numeric
          
54.	**tBodyGyroMag.std..**

          Standard deviation of the magnitude of the body angular velocity
          Type: numeric
          
55.	**tBodyGyroJerkMag.std..**

          Standard deviation of the magnitude of the body Jerk signal, as obtained from the angular velocity 
          Type: numeric

56.	**fBodyAcc.std...X**

          Standard deviation of the FFT of the body acceleration signal in the X direction
          Type: numeric
          
57.	**fBodyAcc.std...Y**

          Standard deviation of the FFT of the body acceleration signal in the Y direction
          Type: numeric
          
58.	**fBodyAcc.std...Z**

          Standard deviation of the FFT of the body acceleration signal in the Z direction
          Type: numeric

59.	**fBodyAccJerk.std...X**

          Standard deviation of the FFT of the body Jerk signal, as obtained from the acceleration, in the X direction
          Type: numeric
          
60.	**fBodyAccJerk.std...Y**

          Standard deviation of the FFT of the body Jerk signal, as obtained from the acceleration, in the Y direction
          Type: numeric
          
61.	**fBodyAccJerk.std...Z**

          Standard deviation of the FFT of the body Jerk signal, as obtained from the acceleration, in the Z direction
          Type: numeric

62.	**fBodyGyro.std...X**

          Standard deviation of the FFT of the body angular velocity in the X direction
          Type: numeric
          
63.	**fBodyGyro.std...Y**

          Standard deviation of the FFT of the body angular velocity in the Y direction
          Type: numeric
          
64.	**fBodyGyro.std...Z**

          Standard deviation of the FFT of the body angular velocity in the Z direction
          Type: numeric

65.	**fBodyAccMag.std..**

          Standard deviation of the magnitude of the FFT of the body acceleration signal 
          Type: numeric
          
66.	**fBodyAccJerkMag.std..**

          Standard deviation of the magnitude of the FFT of the body Jerk signal, as obtained from the acceleration 
          Type: numeric
          
67.	**fBodyGyroMag.std..**

          Standard deviation of the magnitude of the FFT of the body angular velocity
          Type: numeric

68.	**fBodyGyroJerkMag.std..**  

          Standard deviation of the magnitude of the FFT of the body Jerk signal, as obtained from the angular velocity 
          Type: numeric
  
  

  
  
  
  