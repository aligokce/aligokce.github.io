---
name: Transmission of Voice Signals via Acoustic Waves as Communication Medium
tools: [lectures, bachelors]
image: /Screenshot%202025-08-07%20at%2015.59.06.png
description: 2020-01-15
---


## Transmission of Voice Signals via Acoustic Waves as Communication Medium

2020-01-15

EE430 Digital Signal Processing

* * *

In this project, we have designed and implemented a system that will transmit voice from one computer to another by using acoustic waves as the communication medium. The transmitter-side computer captures the voice using a microphone, process it and transmit acoustic waves from its speakers. The receiver-side computer receives the transmitted acoustic waves with its microphone, process it and play back the reconstructed voice from its speakers.

![](/Screenshot%202025-08-07%20at%2015.55.35.png)



From scalar quantisation techniques, we have the following options:

- Uniform quantisation
- Non-uniform quantisation
    - Mu-law
    - A-law
- Lloyd-Max quantisation



Uniform quantisation assumes that sampled signal amplitude is uniformly distributed over the full-scale range. However, exploring speech signals in general, while vowel sounds may span entire scale, softer speech like in consonants, usually have much smaller amplitudes. To comfortably distinguish softer voices, we need more quantisation levels on lower amplitudes compared to high amplitude levels. Non-uniform quantisation offers this property (see [link](https://www.sciencedirect.com/topics/engineering/uniform-quantization "https://www.sciencedirect.com/topics/engineering/uniform-quantization")).



* * *



We used three different types of modulations:

- Frequency-shift keying (FSK)
- Binary phase-shift keying (BPSK)
- Quadrature phase-shift keying (QPSK)



The complexity and the performance (in “certain” terms) of the above modulation types increase from FSK to QPSK.

- M-FSK
    - Advantages
        - Provides high signal-to-noise ratio (SNR)
        - Simple transmitter / receiver design for low data rate applications
    - Disadvantages
        - ■ Increasing M resulting in exponential increase in bandwidth
        - ■ Uses larger bandwidth compared to PSK techniques
        - ■ Higher bit error rate (BER) under AWGN compared to PSK techniques

- BPSK
    - Advantages
        - High robustness to noise and distortion, across all PSK techniques
        - Non-coherent scheme: no reference wave transmission
    - Disadvantages
        - Low data rate: 1 bits/symbol

- QPSK
    - Advantages
        - Uses 4 different phases, high data rates can be achieved: 2 bits/symbol
        - High-data rate with the same bandwidth need of BPSK, or low-data rate with the half bandwidth need
        - Gray coding can be used to reduce the bit error rate
    - Disadvantages
        - Low robustness to distortion



* * *



Loudspeaker are audio devices that amplify the signal power through vibration. This property cause speakers to not being able to immediately stop transmitting. Because even after transmission is stopped through the software, physical vibrations will continue for a while. Although they will be decaying, receiver side microphone will be able to catch them. This problem can be avoided by increasing the bit duration, so that multiple frequency vibrations will not be observed.

Another hardware problem might be the starting delay of the microphones. This physical problem might be avoided by waiting after the starting signal. Since the communication channel will be air, there may be many different paths over which the signal will travel from transmitter to receiver. This may cause high frequency components in the signal and might be avoided by higher bit duration.



![](/Screenshot%202025-08-07%20at%2015.59.06.png)