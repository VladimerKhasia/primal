<div align="center">

# Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning

[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Paper Status](https://img.shields.io/badge/Status-Research_Code-005696?style=flat-square)]()

</div>

<p align="center">
  <strong>Official implementation of the paper "Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning"</strong>
</p>


## Abstract

We present Primal, a deterministic feature mapping framework that harnesses the
number-theoretic independence of prime square roots to construct robust, tunable vector
representations. Diverging from standard stochastic projections (e.g., Random Fourier
Features), our method exploits the Besicovitch property to create irrational frequency
modulations that guarantee infinite non-repeating phase trajectories. We formalize two
distinct algorithmic variants: (1) StaticPrime, a sequence generation method that produces
temporal position encodings empirically approaching the theoretical Welch bound for
quasi-orthogonality; and (2) DynamicPrime, a tunable projection layer for input-dependent
feature mapping.
A central novelty of the dynamic framework is its ability to unify two disparate mathematical utility classes through a single scaling parameter σ. In the low-frequency regime,
the method acts as an isometric kernel map, effectively linearizing non-convex geometries (e.g., spirals) to enable high-fidelity signal reconstruction and compressive sensing.
Conversely, the high-frequency regime induces chaotic phase wrapping, transforming the
projection into a maximum-entropy one-way hash suitable for Hyperdimensional Computing and privacy-preserving Split Learning. Empirical evaluations demonstrate that our
framework yields superior orthogonality retention and distribution tightness compared
to normalized Gaussian baselines, establishing it as a computationally efficient, mathematically rigorous alternative to random matrix projections.

---

## Installation

This repository requires a standard scientific Python stack.

```bash
pip install torch numpy matplotlib seaborn pandas scikit-learn scipy

@article{khasia2025primal,
  title={Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning},
  author={Khasia, Vladimer},
  journal={arXiv preprint},
  year={2025}
}
