---
name: Procedural Sound Generation of Sword Fight Sound Effects in Pure Data
tools: [lectures, masters]
image: /image%205.png
description: 2021-06-18
---


## Procedural Sound Generation of Sword Fight Sound Effects in Pure Data

2021-06-18

MMI522 Procedural Sound Design

* * *

In this project, the objective is to simulate a sword fight between two samurai auditorily by synthesising a number of important sounds within this context and creating control blocks that automatically run a scenario predefined with a small fraction that runs in a random fashion.



There are three main sounds to be synthesised procedurally. The first ones are the sounds of the drawing and the sheathing of a sword. A rectangular metallic lamina is to be modelled in this part. This part takes speed and magnitude into account and is responsible for the state of the sword, whether it is drawn or sheathed. The second is the swinging sound, which is to be created when conditions for a turbulent flow are satisfied. The turbulence condition can be checked by calculating the corresponding Reynolds number, which will later be explained in this report. This part takes the length, thickness, and speed of the sword into account when synthesising. The last is the hit sound of two swords.



For sound synthesis, all subpatches make use of rotating fan blade pulse as the basis oscillator, with varying decorators such as Doppler component and fan noises with different characteristics and controls. These implementations and decorations are referenced from Farnell’s lecture book \[3\]. For draw and hit sounds, the outputs of previously mentioned oscillators are passed to a sequence of bandpass filters, passing six different dominant frequency components in total, which are to be configured later. All sounds are multiplied with an envelope that is tailored for each case, which will later be explored in this section.



### Graphical user interface

![](/image%205.png)

### Fan noise model from the lecture book (see References)

![](/image%206.png)

### Dominant frequency components creation from input fan noise

![](/image%207.png)

### Sample of a metallic sword strike

![](/image%208.png)

![](/image%209.png)![](/image%2010.png)



### References

A. Farnell, _Designing Sound_. MIT Press, 2010.