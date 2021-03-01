# Handover prediction in 5G networks

**Сlient**: International network software provider

**Contractor**: Data Monsters

**Date**: February 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/business_cases/images/img_5G_handover_prediction.png)

### Challenge

Each mobile device in the network is served by a specific base station. When a user moves from one station to another, his device must switch to a new station at some point. This procedure is called a handover. Traditionally, the decision to start a handover is made on the basis of strict rules - for example, when the signal from the new station is stronger than the signal from the old station for a certain time. However, these rules are not always optimal and sometimes the handover leads to signal degradation, or, conversely, the handover does not take too long. The task of the project was to determine the moment of handover based on machine learning algorithms.

### Solution

The collection and preparation of data from mobile devices and service stations were carried out. On the basis of several dozen different parameters contained in the data, features were formed to determine the beginning of a handover. Several ML models were tried, such as linear model, gradient boosting, recurrent and convolutional neural networks, of which the best was chosen.

### Results

A model was developed to predict the signal strength from the old and new station after a given time. This made it possible to predict the appropriate handover moment more accurately, thereby improving the user experience of mobile network users.
