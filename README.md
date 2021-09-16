__Description__
- This dataset is collected from 30 people(referred as subjects in this dataset), performing different activities with a smartphone to their waists. 
- The data is recorded with the help of sensors (accelerometer and Gyroscope) in that smartphone. This experiment was video recorded to label the data manually.
- By using these sensors, the linear acceleration of the body was captured in all the three axes (X-axis, Y-axis, and Z-axis).
- Using these readings, data was labelled munaully for supervised learning task. 

__Problem Statement of this project__
- The objective of this project is to build a model that predicts the human activities such as Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing or Laying using the raw data from sensors. This is a time series problem.

__Model Architecture__
- Used [Divide and Conquer](https://www.mdpi.com/1424-8220/18/4/1055) approach.
- First built a binary classifier model (M_binary) that will classify whether the activity is __Static__ (Sitting, Standing, and Laying) or __Dynamic__ (Walking, Walking_Upstairs, and Walking_Downstairs).
- Then built another two models (M_static and M_dynamic). 
- If M_binary predicts input as static then pass the input to M_static to predict whether the output is Sitting, Standing, or Laying.
- If M_binary predicts input as dynamic then pass the input to M_dynamic to predict whether the output is Walking, Walking_Upstairs, or Walking_Downstairs.

- M_binary
- ![Binary](https://github.com/shashank3009/human-activity-r/blob/main/Model%20Architecture/M_binary.png)

- M_static
- ![Static](https://github.com/shashank3009/human-activity-r/blob/main/Model%20Architecture/M_static.png)

- M_dynamic
- ![Dynamic](https://github.com/shashank3009/human-activity-r/blob/main/Model%20Architecture/M_dynamic.png)

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
