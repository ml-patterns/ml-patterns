# Box Volume Estimation on Packaging Line

**Solution by**: [Data Monsters](www.datamonsters.com)

**Date**: March 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/img_box_volume_estimation.png)

### Challenge

Boxes with contents move along the conveyor, and the empty volume in them is filled with a special filler. The content of each box is different, so it is necessary to calculate the required amount of filler for each box individually, balancing precision, operating speed, and the cost of the equipment.

### Solution

The 3D camera is positioned above the production conveyor. It takes a depth map of a box and its contents. Anomalies and noise are then removed from the image. The neural network deployed to Nvidia Jetson Xavier uses a depth map to calculate the dimensions of a box, as well as the volume of its contents. Based on the data obtained, the required filler volume is calculated.

### Technologies used:

Nvidia Jetson Xavier, Allen Bradley PLC
