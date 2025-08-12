---
name: Predicting Mouse Movements using Kalman Filters via LabVIEW and custom C library in LabWindows/CVI
tools: [lectures, bachelors]
image: /kalman_front_panel.png
description: 2020-06-01
---


## Predicting Mouse Movements using Kalman Filters via LabVIEW and custom C library in LabWindows/CVI

2020-06-01

* * *

This project is about the implementation of Kalman Filter in order to predict the movement of the mouse. Kalman Filter theory is built over the Wiener Filter. One of the main differences between these two filters is the former one has a model which includes the dynamics of the moving object. Hence Kalman Filter is the main tool for estimating the trajectory of moving objects.


Kalman filter has been implemented in C and called from LabVIEW as a shared library function "kalman.so" that should be placed in the appropriate directory of myRIO. Therefore the mouse trajectory predictor runs in myRIO and the predicted mouse position will be displayed in the computer user interface. The input is the current mouse position and the output ise the predicted mouse position.  

The user interface should show the previous mouse trajectory, and the predicted mouse (x, y) coordinate. The current and the predicted mouse coordinates should be shown as blue and red circles respectively in sufficient size. You should also plot the direction vector from the current to the predicted coordinate. The predicted coordinate and the real coordinate should be shown in the user interface as the predicted and the real trajectories. It also shows the least-squares error between the predicted and the real coordinate points in the user interface.



![](/kalman_front_panel.png)



![](/image%2024.png)

![](/kalman_block_diagram.png)

![](/image%2025.png)



