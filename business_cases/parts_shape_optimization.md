# Shape optimization of the device components

**Solution by**: Data Monsters

**Date**: February 2021

![Scheme](url)

### Challenge

When designing various physical devices, it is necessary to minimize the cost of the material while meeting the strength requirements. For this, destructive testing of digital 3D models of device components in physical simulation systems is used. These experiments with manual selection of the parameters of the components are time-consuming. The challenge is to create a tool to automate this routine.

### Solution

A pipeline was developed, including processing the CAD file, automatically running the experiment in the physical simulation system, and optimizing the component parameters using a Bayesian optimization tool. Since the parts of the pipeline are located on different servers, data exchange is carried out using a secure protocol. The user sets experimental parameters such as boundary conditions and cell size, and the system calculates the optimal shape of device components, optimizing material consumption while meeting strength requirements.

### Technologies used

Finite element analysis, Bayesian optimization, Remote procedure call
