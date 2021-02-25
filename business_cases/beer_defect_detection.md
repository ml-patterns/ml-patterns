# Detection of Defects in Aluminum Cans on a Conveyor

**Сlient**: Worldwide beer company

**Contractor**: Data Monsters

**Date**: February 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/business_cases/images/1.jpg)

### Challenge

Detect aluminium cans defects on the packaging line moving at 2 m/s (over 2000 products per minute). The same line is used for different products - the product design is changing several times a day. There is no landline internet connection outside the factory floor. Products are distributed unevenly on the line and are covered with water drops. The defects are rare and there is no dataset of defects.

### Solution

Anomaly-detecting computer vision system based on an ensemble of unsupervised deep learning models. Images are captured by hi-speed still cameras (exposure less than 50 microseconds) and specialized lighting system to avoid blurring and flickering. The images are transferred by high-speed GigE interface to a processing server equipped with 2 NVIDIA T4 GPU cards. The server is managed remotely via the cloud-based edge orchestration system **NVIDIA FleetCommand** using an LTE channel. The models on the server are regularly updated from the cloud. The models are training by observing the flow of products and detecting deviation from the expected product image above certain threshold.

### Business effect

Unknown
