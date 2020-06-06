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

| Optimizer | Train set accuracy | Val set accuracy | Running time (seconds) |
| ------ |:------------------:|:----------------:| :----------------------:|
| Regular SGD | 86.72% | 86.37% | 141.7 |
| SGD with momentum=0.9 | 91.54%      |   88.57% | 154.6 |
| Nesterov Accelerated Gradient | 91.41%      |  89% | 164.2 |
| AdaGrad | 86.59%      |    85.82% | 162.99 |
| RMSProp | 87.53%      |    87.07% | 249.5 |
| Adam | 92.24%      |    89.47% | 193.8 |
| Adamax | 92.91%  | 89.55% | 175.4 |
| Nadam | 92.98%      |    89.55% | 297.4 |
