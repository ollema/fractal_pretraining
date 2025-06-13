## Experiments: Hyperparameter Study

Fractal "complexity" is based on the $\sigma$-factor

Vit-Tiny, data augmentation based on DeiT

| σ-factor | CIFAR-100 | ImageNet-100 |
| -------- | --------- | ------------ |
| 6.0      | 81.3%     | 86.3%        |
| 5.0      | 82.2%     | 87.1%        |
| **3.5**  | **84.2%** | **89.0%**    |

The most "complex" shape yields the highest performance. 

Even with a fractal of $\sigma$ = 6.0, which looks like Gaussian noise, they observed positive pre-training effects.
