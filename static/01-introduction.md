## Disclaimer

Opinions expressed are solely my own and do not express the views or opinions of my employer.

---

## Disclaimer

~Opinions expressed are solely my own and do not express the views or opinions of my employer.~

This paper focuses on image classification tasks, and the findings do not necessarily generalize to other domains.

---

## Introduction: Pre-training

**Current Approach: More Data = More Better**

- ImageNet-1k: 1.3M images
- ImageNet-21k: 14M images
- JFT-300M: 300M images
- Modern foundation models: Billions of images

Traditional hypothesis: Pre-training discovers universal structures in large-scale datasets

---

## Introduction: The Central Question in _Scaling Backwards_

**Do we really need millions of images for pre-training?**

- What if pre-training is just **better weight initialization**?
- Could we achieve similar performance with **minimal data**?
- Can we challenge the "more data = better performance" paradigm?

Bonus: No licensing or bias issues with synthetic data

---

## Spoiler Alert: Scaling Backwards Works?

**1p-frac can outperform pre-training on ImageNet-21k when fine-tuning on ImageNet-1k.**

| Pre-training Dataset | #Images | Type          | ImageNet-1k Acc |
| -------------------- | ------- | ------------- | --------------- |
| Scratch              | -       | -             | 79.8%           |
| ImageNet-21k         | 14M     | Real          | 81.8%           |
| FractalDB-21k        | 21M     | Synthetic     | 81.8%           |
| **1p-frac**          | **1**   | **Synthetic** | **82.1%**       |
