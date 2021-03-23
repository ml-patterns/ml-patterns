# Automatic Detection of Pipeline Defects

**Solution by**: [Artificial Intelligence Institute of Innopolis University](https://innopolis.university/en/)

**Date**: March 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Automatic_Detection_of_Pipeline_Defects.jpg)

### Challenge

A number of diagnostic organizations perform pipeline analysis. For this, a purpose-built robot is launched into the pipeline, which then uses specialized sensors to scan the state of the metal therein. The data is transferred to special devices for further processing and storage. Then, the data is analyzed by diagnostic experts using specialized software. Based on the results of the analysis, a report is generated that indicates the pipe sections, defects, their mechanical characteristics, and the level of danger. Then, a decision is made on the potential replacement of pipes and their further operation. However, the diagnostician is too slow in performing data analysis. The main goal is to replace people with ML algorithms.

### Solution

The information system is based on a microservice architecture. The primary data from the robots is uploaded to the system for further analysis. State-of-the-art computer vision methods are used to detect defects.

### Technologies

PyTorch, NVIDIA TensorRT, RabbitMQ, Kafka, Docker