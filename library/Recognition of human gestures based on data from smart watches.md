# Recognition of human gestures based on data from smart watches

**Solution by**: [MIL Team](https://machine-intelligence.ru/en/mil-team)

**Date**: September 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Recognition_of_human_gestures_based_on_data_from_smart_watches.jpeg)

### Challenge

The task was to determine the number and frequency of certain human actions using data from the inertial sensors of smartwatches and fitness trackers, revealing, for example, the number of cups of coffee drunk or the number of cigarettes smoked.

### Solution

First, the assessors performed segmentation and classification of human actions based on information from the video. Before labeling the video, we carried out data anonymization and pre-labeling of the initial data using pose estimation models. Upon labeling a small part of the sample (10%), we built a model for automatic data labeling based on the video stream in order to speed up the labeling process.
The labeled video was then used to train a gesture recognition model based on data from inertial sensors. We used an unsupervised method for synchronizing the video sequence and the smartwatch data. The final recognition model was trained on the synchronized automatic labeled and sensor data.

### Technologies

- Pose estimation models on the video stream and face detection models
- RNN models for segmentation and classification of IMU data;
- Python
- PyTorch;
- In-house development of methods for processing data from inertial sensors.
