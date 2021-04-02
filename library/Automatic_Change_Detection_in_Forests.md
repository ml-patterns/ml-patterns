# Automatic Change Detection in Forests

**Solution by**: [Artificial Intelligence Institute of Innopolis University](https://innopolis.university/en/)

**Date**: March 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Automatic_Change_Detection_in_Forests.jpeg)

### Challenge

To preserve the environment, the government must monitor forests and respond quickly to events such as fires or illegal logging. Since the overall forest area is huge, it is very expensive to check every part of it in real time using human labor.

### Solution

We’ve implemented an automatic system that uses contemporary satellite imagery data of medium resolution (10–15 meters) for change detection. Currently, the system is capable of determining 5 classes of changes: deforestation, fire, quarry development, windfall, and forest pathology. The whole process is automated: the user has only to specify the area of interest (AOI) and the rest will be done by our system. Raw images are downloaded from several possible resources, preprocessed, and then the data is fed to the segmentation algorithms. The system is designed using microservice architecture — tasks are transferred through message brokers such as RabbitMQ. Our solution allows for a decrease in the time needed for monitoring from several man-days per 150 km2 (one satellite image), to several minutes, and is easy to scale. This is an example of a true breakthrough thanks to artificial intelligence algorithms.

### Technologies

PyTorch, RabbitMQ, Redis, Docker, Kubernetes.
