# DNN-Improvement
Techniques to improve DNN performance usign Fashion MNIST as example.

## Part 1: Initialization strategies, Activation function, and Batch normalization

---
#### Summary performance of Classification task with ```Fashion MNIST``` dataset

| Initialization | Activation fuction | Train set accuracy | Val set accuracy | Running time (seconds) |
| ------ |:------:|:------------------:|:----------------:| :----------------------:|
| Glorot | No Activation | 85.32% | 84.95% | 104.5 |
| Glorot - Normal Dist | ReLU | 85.26%      |   85.18% | 99.03 |
| **He - Normal Dist** | **ReLU** | **86.72%**      |  **86.37%** | **99.76** |
| He - Uniform  Dist | ReLU | 87.05%      |    86.27% | 100.82 |
| He - Normal  Dist | Leaky ReLU | 86.7%      |    86.15% | 101.87 |
| He - Normal  Dist | Randomized LeakyReLU | 86.67%      |    86.3% | 113.58 |
| **LeCun** | **SELU** | **87.63%**  | **86.47%** | **106.25** |
| Batch normalization He - Normal  Dist | ReLU | 86.45%      |    86.85% | 167.618 |


#### Summary performance of Regression task with ```California housing``` dataset

| Initialization | Activation fuction | Train set MSE | Val set MSE | Running time (seconds) |
| ------ |:------:|:------------------:|:----------------:| :----------------------:|
| Glorot | No Activation | 0.3985 | 0.3899 | 9.34 |
| Glorot - Normal Dist | ReLU | 0.3779 |  0.3819 | 9.36 |
| He - Normal Dist | ReLU | 0.3517 |  0.35 | 9.19 |
| He - Normal  Dist | Leaky ReLU | 0.3517   |   0.35 | 9.48 |
| He - Normal  Dist | Randomized LeakyReLU | 0.3517  | 0.35 | 10.71 |
| **LeCun** | **SELU** | **0.3423**  |  **0.326** | **9.38** |
| Batch normalization He - Normal  Dist | ReLU | 0.4365 | 0.5728 | 13.64 |

---

## Part 2: Tune Optimizer, Learning rate, and Dropout

---
#### Summary performance of Classification task with ```Fashion MNIST``` dataset using He Initialization and ReLU activation function

*Running time is not comparable with Part 1*

| Optimizer | Train set MSE | Val set MSE | Running time (seconds) |
| ------ |:------------------:|:----------------:| :----------------------:|
| Regular SGD | 86.74% | 86.2% | 99.7 |
| SGD with momentum=0.9 | 92.1%      |   88.5% | 105.1 |
| **Nesterov Accelerated Gradient** | **92.2%**      |  **88.9%** | **112.2** |
| AdaGrad | 86.59%      |    85.83% | 113.6 |
| RMSProp | 88.08%      |    84.6% | 158.7 |
| Adam | 92.9%      |    89.73% | 126.8 |
| Adamax | 93.7%  | 88.8% | 119.04 |
| **Nadam** | **93.14%**      |    **89.3%** | **204.2** |


#### Summary performance of Regression task with ```California housing``` dataset using He Initialization and ReLU activation function

| Optimizer | Train set MSE | Val set MSE | Running time (seconds) | Epoch |
| ------ |:------------------:|:----------------:| :------------:|:---------:|
| Regular SGD | 0.3517 | 0.35 | 13.06 | 20 |
| SGD with momentum=0.9 | 0.3038      |  0.3012 | 13.68 | 19 |
| Nesterov Accelerated Gradient | 0.3125      |  0.305 | 13.3 | 15 |
| AdaGrad | 0.5317     |    1.2473 | 13.84 | 20 |
| RMSProp | 0.2453    |    0.278 | 26.8 | 36 |
| **Adam** | **0.2374**    |    **0.27** | **33.77** | **40** |
| Adamax | 0.2671  | 0.2758 | 26.94 | 39 |
| **Nadam** | **0.2417**   |    **0.2631** | **31.47** | **36** |
