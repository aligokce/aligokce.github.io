---
name: Comparison of Quantization Techniques for Speech Encoding in PCM
tools: [lectures, bachelors]
image: /Part3_NonUni_Perf.png
description: 2018-04-22
---


# Performance Anaylsis and Comparison of Different Scalar Quantization Techniques for Speech Encoding in Pulse Code Modulation (PCM) Telephony

2018-04-22

EE230 Probability and Random Variables

* * *

In my 2nd year in Bachelor's, for EE230 Probability and Random Variables course, I analysed different quantization techniques for speech encoding, that converts an analog signal, which is mostly a human speech in the case of telephony, into a digital signal.

These are:

- Uniform Quantizer
- Non-uniform Quantizer with Companding Circuitry
    - mu-law, used in the US and Japan
    - A-law, used in EU
- Lloyd-Max Quantizer



{% include elements/figure.html image="Part3_NonUni_Perf.png" caption="Figure: Comparison of companding characteristics of mu- and A-law" %}



{% include elements/figure.html image="part1_amp.png" caption="Figure: Speech signal used in the analyses" %}





![](/Part3_PMF_A.png)

![](/Part3_PMF_mu.png)





![](/Part4_Error.png)