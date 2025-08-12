---
name: Comparison of Model Quantisation Techniques in PyTorch
tools: [lectures, masters]
description: 2022-01-25
---


## Comparison of Model Quantisation Techniques in PyTorch

2022-01-25

MMI712 Machine Learning Systems Design and Deployment

* * *



A wide variety of application areas, hardware capabilities for inferencing tasks using deep neural networks raises the need for model compression - harder, better, and more stable, every day.

Below are two survey papers presented with power points on quantization and pruning.

_From the paper “A Survey of Model Compression and Acceleration for Deep Neural Networks”_ \[1\]:

·       "There are no golden criteria to measure which approach is the best. How to choose a proper method really depends on the applications and requirements."

·       Pruning and quantization are effective in lowering the complexity of neural networks and addresses the over-fitting problem. \[2\]

·       Pruning and quantization generally introduce an acceptable compression while not decreasing the accuracy much.

·       8-bit quantization of parameters can significantly improve speed of DNN models with minimal loss of accuracy. \[3\]

·       A method that achieved the state-of-art performance on quantization proposes quantizing link weights, using weight sharing, and then applying Huffman coding to both the quantized weights and the codebook as well. \[4\]

·       Pruning has an effect of regularizing neural networks, improving generalization capabilities of models.

·       Pruning is an effective way to compress and accelerate CNNs.

·       Early works in network pruning are based on magnitude, Hessian of the loss function to be applied to the weights.

·       Sparsity constrained DNNs are also gaining interest.

_From the paper “A Survey of Quantization Methods for Efficient Neural Network Inference”_ \[5\]:

·       Pruning methods can be casually separated into two categories: unstructured and structured.

·       Unstructured pruning is done by removing neurons with little sensitivity, while leading to sparse matrix operations which are hard to accelerate.

·       Structured pruning, on the other hand, is done by removing a group of parameters, allowing dense matrix operations. However, these methods tend to significantly hurt the accuracy.

·       In Post Training Quantization, all weights and activations quantization parameters are determined without any re-training of the DNN models. While it is a very fast method doing so, it also comes at the cost of lower accuracy, as compared to Quantization Aware Training.

·       Quantization Aware Training needs re-training for many epochs to recover the accuracy under low precision, which may be viable if the model is going to be deployed for an extended period.

* * *



·       _vgg16\_bn_ is used for all experiments. VGG16 is a convolutional network for classification and detection tasks. Its proposal paper used ImageNet as the dataset. It can be slow to train, and the weights are very large. However, it is easy to implement for it makes use of operations that are commonly used, and the flow is straightforward.

·       Quantization methods of PyTorch is used for model compression. Post Training Static Quantization, Post Training Dynamic Quantization and Quantization Aware Training methods are experimented for aforementioned model.

Results for different types of quantization using PyTorch native utilities.

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| **Quantization** | **Test accuracy (%)** | **Inference time (s)** | **Relative time** | **Model size (MB)** |
| **No quantization****vgg16\_bn** | 94.00 | 29.41 | 1   | 134.65 |
| **Post Training Dynamic Quantization**_Default – nn.Linear only – qint8_ | 93.99 | 29.466 | 1.044153 | 77.91 |
| **Post Training Static Quantization**_Default “fbgemm” config_ | 9.99 | 15.48 | 0.548547 | 33.99 |
| **Post Training Static Quantization**_Custom Observers  (act:MinMax, wei:Histogram)_ | 9.99 | 13.79 | 0.488661 | 33.99 |
| **Quantization Aware Training**_Default “fbgemm” config - 100 Epochs_ | 93.75 | 15.20 | 0.538625 | 33.99 |



* * *



### Hardware specs

·       Intel Core i7-10870H @ 2.20 GHz (16 CPUs)

·       32768 MB RAM

·       Windows 10 (10.0 Build 19044)

·       Docker version 20.10.11, build dea9396

·       NVIDIA NGC Container nvcr.io/nvidia/pytorch:21.11-py3

o   NVIDIA Driver 510.00

o   CUDA 11.6

o   Python 3.8.2

### Library versions

·       pytorch\_lightning == 1.4.0

·       requests == 2.26.0

·       torch == 1.11.0a0+b6df043

·       torchmetrics == 0.7.0

·       torchvision == 0.11.0a0

·       tqdm == 4.62.3

### References

\[1\] Y. Cheng, D. Wang, P. Zhou, en T. Zhang, “A Survey of Model Compression and Acceleration for Deep Neural Networks”, arXiv \[cs.LG\]. 2020.

\[2\] Y. Gong, L. Liu, M. Yang, and L. D. Bourdev, “Compressing deep convolutional networks using vector quantization,” CoRR, vol. abs/1412.6115, 2014.

\[3\] S. Gupta, A. Agrawal, K. Gopalakrishnan, and P. Narayanan, “Deep learning with limited numerical precision,” in Proceedings of the 32Nd International Conference on International Conference on Machine Learning - Volume 37, ser. ICML’15, 2015, pp. 1737–1746.

\[4\] S. Han, H. Mao, and W. J. Dally, “Deep compression: Compressing deep neural networks with pruning, trained quantization and huffman coding,” International Conference on Learning Representations (ICLR), 2016.

\[5\] A. Gholami, S. Kim, Z. Dong, Z. Yao, M. W. Mahoney, en K. Keutzer, “A Survey of Quantization Methods for Efficient Neural Network Inference”, arXiv \[cs.CV\]. 2021.