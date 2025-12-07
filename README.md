<div align="center">

# Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning


</div>

<p align="center">
  <strong>Implementation of the paper "Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning"</strong>
</p>

[![arXiv](https://img.shields.io/badge/arXiv-2511.20839-b31b1b.svg)](https://arxiv.org/abs/2511.20839)

## Abstract

We present **Primal**, a deterministic feature mapping framework that harnesses the number-theoretic independence of prime square roots to construct robust, tunable vector representations. Diverging from standard stochastic projections (e.g., Random Fourier Features), our method exploits the *Besicovitch property* to create irrational frequency modulations that guarantee infinite non-repeating phase trajectories.

We formalize two distinct algorithmic variants: **StaticPrime**, a sequence generation method that produces temporal position encodings empirically approaching the theoretical Welch bound for quasi-orthogonality; and **DynamicPrime**, a tunable projection layer for input-dependent feature mapping.

A central novelty of the dynamic framework is its ability to unify two disparate mathematical utility classes through a single scaling parameter $\sigma$. In the *low-frequency regime*, the method acts as an isometric kernel map, effectively linearizing non-convex geometries to enable high-fidelity signal reconstruction. Conversely, the *high-frequency regime* induces chaotic phase wrapping, transforming the projection into a maximum-entropy one-way hash suitable for Hyperdimensional Computing and privacy-preserving Split Learning.

Empirical evaluations demonstrate that Primal yields superior orthogonality retention and distribution tightness compared to normalized Gaussian baselines, establishing it as a computationally efficient, mathematically rigorous alternative to random matrix projections.

---

## Installation

```bash
pip install torch numpy matplotlib seaborn pandas scikit-learn scipy
```

### Experiment Manifest

To reproduce the results, navigate to the `experiments/` folder. The notebooks correspond directly to the figures in the paper:

| Notebook | Objective | Paper Figure |
| :--- | :--- | :--- |
| **`static.ipynb`** | **StaticPrime.** Tightness and RMS error. | **Fig. 1** |
| **`static_detailed.ipynb`** | **StaticPrime.** Distribution of optimality ratios and excess coherence. | **Fig. 2** |
| **`dynamic_regimes.ipynb`** | **DynamicPrime.** High-low frequency regimes. | **Fig. 3** |
| **`represent_classify.ipynb`** | **DynamicPrime.** Representation and classification capacity. | **Fig. 4 & 5** |

---

## Implementation Details

**Note on Determinism and Prime Calculation**

In the associated manuscript, the methodology may reference a pre-computed lookup table for computational efficiency. However, to ensure this repository remains **standalone and lightweight**, the code calculates prime numbers dynamically on-the-fly.

---

## Citation

If you utilize this code or the concepts presented in **Primal** for your research, please cite the following paper:

```bibtex
@article{khasia2025primal,
  title={Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning},
  author={Khasia, Vladimer},
  journal={arXiv preprint	arXiv:2511.20839},
  year={2025}
}
```
