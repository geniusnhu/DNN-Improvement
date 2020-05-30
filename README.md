# DNN-Improvement
Techniques to improve DNN performance usign Fashion MNIST as example.

---
Summary performance of different Initialization strategies, Activation function, and Batch normalization

| Initialization | Activation fuction | Train set accuracy | Val set accuracy | Running time (seconds) |
| ------ |:------:|:------------------:|:----------------:| :----------------------:|
| Glorot | No Activation | 85.32% | 84.95% | 104.5 |
| Glorot - Normal Dist | ReLU | 85.26%      |   85.18% | 99.03 |
| He - Normal Dist | ReLU | 86.72%      |    86.37% | 99.76 |
| He - Uniform  Dist | ReLU | 87.05%      |    86.27% | 100.82 |
| He - Normal  Dist | Leaky ReLU | 86.7%      |    86.15% | 101.87 |
| He - Normal  Dist | Randomized LeakyReLU | 86.67%      |    86.3% | 113.58 |
| LeCun | SELU | 87.63%      |    86.47% | 106.25 |
| Batch normalization He - Normal  Dist | ReLU | 86.45%      |    86.85% | 167.618 |
