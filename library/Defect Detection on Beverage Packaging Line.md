# Defect Detection on Beverage Packaging Line

**Solution by**: Data Monsters

**Date**: February 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/beverage_defects_detection.jpeg)

### Challenge

Detecting aluminium can defects on the packaging line moving at 2 m/s (with over 2000 products per minute). The same line is used for different products — the product design changes several times a day. There is no landline internet connection outside the factory floor. Products are distributed unevenly on the line, and are covered with water drops. The defects are rare and there is no dataset of defects.

### Solution

An anomaly-detection computer vision system based on an ensemble of unsupervised deep learning models. Images are captured by hi-speed still cameras (at an exposure of less than 50 microseconds), and a specialized lighting system to avoid blurring and flickering. The images are transferred by high-speed GigE interface to a processing server equipped with 2 NVIDIA T4 GPU cards. The server is managed remotely via the cloud-based edge orchestration system **NVIDIA FleetCommand** using an LTE channel. The models on the server are regularly updated from the cloud. The models are trained by observing the flow of products and detecting any deviation from the expected product image above a certain threshold.

### Technologies used

NVIDIA DeepStream, NVIDIA FleetCommand, PyTorch, Kafka
