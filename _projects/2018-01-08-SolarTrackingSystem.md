---
name: Solar Tracking System
tools: [lectures, bachelors]
image: /213_photo.jpg
description: 2018-01-08
---


# Solar Tracking System

2018-01-08

EE213 Electrical Circuits Laboratory

* * *

{% include elements/figure.html image="213_photo.jpg" caption="Photo: Prototype on a single piece of breadboard" %}



In my 2nd year of Bachelor's, I designed a solar tracking system that tracks the light intensity of different angles and makes the imagined solar panel rotate to the angle which the incoming light is the brightest. The principle is to get better efficiency in transforming solar energy into electricity.



This project consists of three main units: sensing, control, and angle adjustment units.

Figure: A high level block diagram of the project design.

![](https://dvqlxo2m2q99q.cloudfront.net/000_clients/1193912/file/1193912waEMD5sm.png)



Sensing unit gathers the data in voltage form and sends it to the control unit. Control unit compares these data and generates a corresponding pulse width modulation (PWM) signal. Then, angle adjustment unit uses this signal to adjust the angle of the servo motor. Thus, the panel is faced to the direction of most intense light.



{% include elements/figure.html image="213_circuit.jpg" caption="Figure: Circuit design of the project" %}