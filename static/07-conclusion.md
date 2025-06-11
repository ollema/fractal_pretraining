## Conclusion: Key Contributions

The key contributions of this work according to the authors:

**1. Ordinal Minimalism**
- Single fractal matches 14M image datasets
- Challenges "more data = more performance" paradigm

**2. Distributional Minimalism**  
- Performance driven by "imperceptible" perturbations
- In other words, networks learn from differences humans cannot distinguish

**3. Instance Minimalism**
- Structure matters: fractals work, noise fails
- Real images can scale backwards with edge enhancement + affine transforms

---

## Conclusion: Scaling Backwards

Real images scale with the dataset size

| 1 | 1k | 1M |
|---|----|----|
| N/A | 76.9% | 85.5% |

Synthetic images scale backwards in this paper:

| 1M | 1k | 1 |
|----|----|----|
| 81.6% | 84.0% | 84.2% |


---

## Conclusion: Why Does This Work?

**Pre-training as optimization, not concept learning**

Traditional hypothesis: Pre-training learns universal visual concepts

New hypothesis: Pre-training may primarily improve weight initialization

Given:
- Minimal synthetic data achieves comparable performance
- Geometric transformations matter more than semantic content  

(Remember the initial disclaimer)

---

## Conclusion: Impact

Matches ImageNet-21k on ImageNet-1k fine-tuning (82.1% vs 81.8%)

Superior early layer representations (linear probing)

No licensing or bias concerns

Opens the possibility for gains in training speed by keeping the data on the GPU

---

## Conclusion: Limitations

**Current limitations:**
- Focused on image classification tasks
- Limited to moderate model sizes

**Future work:**
- Extend to other tasks
- Scale to other/larger model architectures
