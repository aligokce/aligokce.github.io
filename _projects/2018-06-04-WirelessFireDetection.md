---
name: Wireless Fire Detection System
tools: [lectures, bachelors]
image: /1193912VLNW8plU.jpg
description: 2018-06-04
---


# Wireless Fire Detection System

2018-06-04

EE214 Electronic Circuits Laboratory

* * *

In my 2nd year in Bachelor’s on Electrical and Electronics Engineering, I designed a wireless fire detection system for the Electrical Circuits Laboratory II. It basically gets the temperature data from its sensors, transmits this information via sound, and an LED is switched on at the receiver end, representing the detection.



{% include elements/figure.html image="1193912VLNW8plU.jpg" caption="Photo: Transmitter and receiver prototypes on breadboards, which are physically separate except the power lines here" %}



The system gathers temperature information from its sensing unit, consists of sensors, comparators a decision sub-unit. After the system decides which sensor is the hottest, it creates a waveform with a frequency that is assigned to each location. Then, this waveform is sent to the transmission unit which features a Class AB amplifier that powers up a speaker. The sound is transformed into a voltage waveform via a microphone, which will later be sent to the indicator unit. This unit makes sense of the incoming sound using band-pass and then enlightens the LED corresponding to the hottest location.

The whole circuitry design is as seen below.



{% include elements/figure.html image="119391289MoN3na.png" caption="Figure: Circuit design of the project" %}