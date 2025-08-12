---
name: Photophone, An Optical Wireless Communication System
tools: [lectures, bachelors]
image: /1193912wh8vPXt1.jpg
description: 2019-01-22
---


# Photophone: Design of an Optical Wireless Communication System

2019-01-22

* * *

In my 3rd year in Bachelor's, I designed an optical wireless communication system for Analog Electronics Laboratory. This is a modified version of Bell's [photophone](https://en.wikipedia.org/wiki/Photophone) using electrical modulation of transmitted light. The design only consists of analog electronic components.



{% include elements/figure.html image="1193912wh8vPXt1.jpg" caption="Photo: Prototype circuit on a single piece of breadboard" %}

The system gathers the surrounding sound via a microphone and applies _Automatic Gain Control_ to ensure the audibility of any dominant sound. Then, it is summed with a constant reference signal (_see:_ [multiplexing](https://en.wikipedia.org/wiki/Multiplexing)). Then, a laser transmits the modified sound to a receiver, which is a photodiode. This signal is separated and converted back into the speech signal and reference signal (demultiplexing). Additionally, the system also features a volume controller, a clipping check, a _signal level indicator_, a speaker switch for the times when the signal is too poor, and a Class AB power amplifier.



Video: Presenting the inner workings of the project.

[EE313 Project Video: Photophone](https://www.youtube.com/embed/NaXRuTny5Yo?feature=oembed "EE313 Project Video: Photophone")
{% include elements/video.html id="NaXRuTny5Yo" %}


{% include elements/figure.html image="1193912nowufFT6.png" caption="Figure: Block diagram of transmitter and receiver units" %}



{% include elements/figure.html image="11939126pdpL0JD.png" caption="Figure: Modular circuit design for the project" %}