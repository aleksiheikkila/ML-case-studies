### Using smartphone accelerometers and gyroscopes time series data for activity classification

The use case here is classifying Human Activity Recognition (HAR) using windowed time series data collected from accelerometers and gyroscopes of a smartphone. 

### Dataset

Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors: accelerometers and gyroscoped (accelerometers measure linear accelerations, gyros give the rotational/angular velocities).

The data is from experiments carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity were captured at a constant rate of 50Hz. 

The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (thus 128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

So, in a nutshell, the data contains 9 different variables:
 - total acceleration (in 3 directions/axes)
 - body acceleration (in 3 directions/axes)
 - body gyroscope (in 3 directions/axes)

Each with a measured value every 0.05s. The data is split into windows of 2.56s, and these are the input data samples. So, each input data sample is of shape (128, 9), i.e. 128 "time steps" for 9 variables.

For more detailed dataset description, see [here](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones).

### Task

The measurement data, i.e. each window of 2.56s with 9 variables, need to be mapped into 6 different basic activities (Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying).


### Approach

Traditionally, the approach for HAR has been heavy on feature engineering. Here I apply deep learning for the task, with minimal feature engineering.

Models used are based on LSTM architecture. I did not search for optimize the hyperparameters too much 

I played the model selection by ear, not being very methodological in searching the "best" architecture or its parameters. I tried e.g. stacked (two LSTMs back-to-back) and non-stacked (single) LSTM, bi- and unidirectional versions, and different settings for bias/weight regularizers and dropout rates.
