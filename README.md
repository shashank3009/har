# har
__Problem Statement__
- The objective of this project is to build a model that predicts the human activities such as Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing or Laying.

__Description__
- This dataset is collected from 30 persons(referred as subjects in this dataset), performing different activities with a smartphone to their waists. 
- The data is recorded with the help of sensors (accelerometer and Gyroscope) in that smartphone. This experiment was video recorded to label the data manually.
- By using these sensors, the linear acceleration of the body was captured in all the three axes (X-axis, Y-axis, and Z-axis).
- Using these readings, data was labelled munaully for supervised learning task. 

__Labels__

- WALKING as 1
- WALKING_UPSTAIRS as 2
- WALKING_DOWNSTAIRS as 3
- SITTING as 4
- STANDING as 5
- LAYING as 6

__Note__
- Readings are divided into a window of 2.56 seconds with 50% overlapping.
- Accelerometer readings are divided into gravity acceleration and body acceleration readings, which has x,y and z components each.
- Gyroscope readings are the measure of angular velocities which has x,y and z components.
