---
name: Pinball, An FPGA Game Over VGA
tools: [lectures, bachelors]
image: /1193912eSIS82Du.jpg
description: 2019-06-15
---


# Pinball: An FPGA Game Over VGA

2019-06-15

EE314 Digital Circuits Laboratory

* * *

In my 3rd year on Electrical and Electronics Engineering in METU, me and my project partner, designed a pinball game that works on a De1-SoC FPGA board. The game is written in Verilog HDL. It consists of all basic elements of a pinball game: targets, boundaries, flippers, plunger, timer and a scoreboard. The game is playable via buttons on the FPGA board.



{% include elements/figure.html image="1193912eSIS82Du.jpg" caption="Photo: Final working game product" %}



Video: Me and my project partner, explaining the inner schemes of our Pinball game design for FPGA.

[EE314 Digital Electronics Laboratory Project: Pinball](https://www.youtube.com/embed/GhElB6Vg3u0?feature=oembed "EE314 Digital Electronics Laboratory Project: Pinball")
{% include elements/video.html id="GhElB6Vg3u0" %}


This project consists of two main parts: VGA communication for display purposes, and the overall mechanics and design of the game.



Source codes of the project consists of many modules:

1. VGA
2. boundary
3. flipper
4. circle
5. hexagon
6. ball
7. collision
8. bcd (binary coded decimal)
9. number\_display
10. timer



{% include elements/figure.html image="1193912AzEs3TsB.png" caption="Photo: The FPGA board used in this project for game engine, controls and VGA video output" %}



{% include elements/figure.html image="1193912AqZGPXsH.png" caption="Figure: Early design plan of the gameplay screen" %}