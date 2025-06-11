## Comprehensive Evaluation

### Performance across 7 diverse datasets

**Datasets:** CIFAR-10/100, Cars, Flowers, Pascal VOC, Places-30, ImageNet-100

**Baselines:** Real images (SL), Self-supervised (SSL), Synthetic (FDSL)

**Key result:** 1p-frac competitive across all domains

---

## Main Comparison Results

### 1p-frac vs everything else (Mean accuracy)

| Method             | #Images | Type     | Mean Accuracy |
| ------------------ | ------- | -------- | ------------- |
| ImageNet-1k (MAE)  | 1.28M   | SSL      | 88.5%         |
| OFDB-1k w/ Aug     | 1k      | FDSL     | 88.5%         |
| **1p-frac w/ Aug** | **1**   | **FDSL** | **88.2%**     |
| 1-image SSL (MAE)  | 1       | SSL      | 86.6%         |
| **1p-frac**        | **1**   | **FDSL** | **87.5%**     |

**Remarkable:** Single fractal nearly matches million-image performance!

---

## VTAB Specialized Datasets

### Performance on domain-specific tasks

| Dataset     | Task Type  | ImageNet-1k | 1p-frac | Gap   |
| ----------- | ---------- | ----------- | ------- | ----- |
| Retinopathy | Medical    | 79.1%       | 77.9%   | -1.2% |
| Resisc45    | Aerial     | 97.0%       | 95.8%   | -1.2% |
| Camelyon    | Pathology  | 82.7%       | 82.7%   | 0.0%  |
| CLEVR-Count | Synthetic  | 89.3%       | 86.2%   | -3.1% |
| sNORB-Azim  | 3D Objects | 29.2%       | 28.9%   | -0.3% |

**Finding:** Competitive even on specialized domains!
