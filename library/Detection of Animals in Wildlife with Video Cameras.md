# Detection of Animals in Wildlife with Video Cameras

**Solution by**: Data Monsters

**Date**: March 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Detection_of%20Animals_in_Wildlife_with_Video_Cameras.jpg)

### Challenge

In the wild, video cameras are installed to monitor the environment. Most of the time, nothing happens in their field of vision. The task is to automatically detect the moments when an animal appears in the field of view of the camera, determine what kind of animal it is, and send a notification and a video fragment to subscribers. Cameras are installed in places with a poor internet connection, so calculations must be performed on the edge.

### Solution

The signal from the video camera goes to NVIDIA Jetson Nano and is split into frames, after which common animals such as deer, elk, fox, and others are detected in real-time. If an animal is found, the message is sent to subscribers using the Firebase Cloud Messaging platform. Rebroadcasting of video from cameras is carried out using the Dacast streaming video platform.

### Technologies used

NVIDIA Jetson Nano, NVIDIA DeepStream SDK, Tensor RT
