<div align="center">

# Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning

[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Paper Status](https://img.shields.io/badge/Status-Research_Code-005696?style=flat-square)]()

</div>

<p align="center">
  <strong>Implementation of the paper "Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning"</strong>
</p>


## Abstract

We present **Primal**, a deterministic feature mapping framework that harnesses the number-theoretic independence of prime square roots to construct robust, tunable vector representations. Diverging from standard stochastic projections (e.g., Random Fourier Features), our method exploits the *Besicovitch property* to create irrational frequency modulations that guarantee infinite non-repeating phase trajectories.

We formalize two distinct algorithmic variants: **StaticPrime**, a sequence generation method that produces temporal position encodings empirically approaching the theoretical Welch bound for quasi-orthogonality; and **DynamicPrime**, a tunable projection layer for input-dependent feature mapping.

A central novelty of the dynamic framework is its ability to unify two disparate mathematical utility classes through a single scaling parameter $\sigma$. In the *low-frequency regime*, the method acts as an isometric kernel map, effectively linearizing non-convex geometries to enable high-fidelity signal reconstruction. Conversely, the *high-frequency regime* induces chaotic phase wrapping, transforming the projection into a maximum-entropy one-way hash suitable for Hyperdimensional Computing and privacy-preserving Split Learning.

Empirical evaluations demonstrate that Primal yields superior orthogonality retention and distribution tightness compared to normalized Gaussian baselines, establishing it as a computationally efficient, mathematically rigorous alternative to random matrix projections.

---

## Installation

This repository requires a standard scientific Python stack.

```bash
pip install torch numpy matplotlib seaborn pandas scikit-learn scipy
```

## Repository Structure & Reproducibility

The codebase is organized to facilitate the reproduction of the specific figures and claims presented in the manuscript. All core experiments are located in the `experiments/` directory.


### Experiment Manifest

To reproduce the results, navigate to the `experiments/` folder. The notebooks correspond directly to the figures in the paper:

| Notebook | Objective | Paper Figure |
| :--- | :--- | :--- |
| **`static.ipynb`** | **Baseline Comparison.** Evaluates Primal against Gaussian Random Projections, analyzing log-distribution landscapes and RMS error. | **Fig. 1** |
| **`static_detailed.ipynb`** | **Theoretical Bounds.** Validates Welch optimality ratios, residuals, and distribution tightness in the static regime. | **Fig. 2** |
| **`dynamic_regimes.ipynb`** | **Manifold Reconstruction.** Demonstrates forward/backward invertibility across scaling regimes using topological datasets (Spiral/Circle). | **Fig. 3** |
| **`represent_classify.ipynb`** | **Latent Separability.** Analyzes class separability retention under noise via Cosine Similarity matrices. | **Fig. 4 & 5** |

To run an experiment:
```bash
cd experiments
jupyter notebook
# Select the desired notebook from the interface
```

---

## Implementation Details

**Note on Determinism and Prime Calculation**

In the associated manuscript, the methodology may reference a pre-computed lookup table for computational efficiency. However, to ensure this repository remains **standalone and lightweight**, the code calculates prime numbers dynamically on-the-fly.

This implementation decision ensures:
1.  No external data dependencies or large file downloads.
2.  Statistically identical results to the lookup table method described in the paper.

---

## Citation

If you utilize this code or the concepts presented in **Primal** for your research, please cite the following paper:

```bibtex
@article{khasia2025primal,
  title={Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning},
  author={Khasia, Vladimer},
  journal={arXiv preprint},
  year={2025}
}
```

## License

This project is licensed under the MIT License.
```

