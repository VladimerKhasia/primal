# Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning

[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Paper Status](https://img.shields.io/badge/Status-Research_Code-blue?style=for-the-badge)]()

This repository contains the official implementation for the paper **"Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning."**

**Primal** introduces a deterministic method using prime number frequencies to generate high-dimensional embeddings. It bridges the gap between static hashing (for orthogonality) and dynamic manifold learning (for reconstruction).

---

## 📂 Repository Structure

The core experiments are located in the `experiments/` directory. Each notebook corresponds to specific figures and claims made in the paper.

| Notebook File | Description | Paper Figures |
| :--- | :--- | :--- |
| **`static.ipynb`** | **Baseline Comparisons.** Compares Primal against Random Gaussian baselines regarding log-distribution landscapes and RMS error. | **Figure 1** |
| **`static_detailed.ipynb`** | **Welch Bounds & Optimality.** A deep dive into the static regime, analyzing Welch optimality ratios, residuals, and distribution tightness. | **Figure 2** (+ Fig 1 details) |
| **`dynamic_regimes.ipynb`** | **Reconstruction & Regimes.** Demonstrates the forward/backward capabilities (invertibility) of the method across low and high-dimensional scaling regimes using Spiral/Circle datasets. | **Figure 3** |
| **`represent_classify.ipynb`** | **Representation Learning.** Analyzes the model's ability to maintain class separability (Spirals vs. Circles) under noise via Cosine Similarity matrices. | **Figure 4 & 5** |

---

## ⚡ Implementation Note

> **Note on Prime Calculation:**
> Unlike the description in the paper—which may reference a pre-computed lookup table for efficiency—this codebase **calculates prime numbers dynamically** on-the-fly.
>
> This ensures the code is standalone and requires no external data files, while producing statistically identical results to the lookup table method.

---

## 🚀 Getting Started

### 1. Prerequisites
The code relies on standard data science and deep learning libraries. You can install the requirements via pip:

```bash
pip install torch numpy matplotlib seaborn pandas scikit-learn scipy
```

### 2. Running the Experiments
Navigate to the experiments folder and launch Jupyter:

```bash
cd experiments
jupyter notebook
```

Select any `.ipynb` file to reproduce the corresponding figure.

---

## 📊 Visualizations

The code generates detailed visualizations comparing the **Primal** method to stochastic baselines.

*   **Static Analysis:** 3D landscapes showing how Primal achieves tighter orthogonality (lower RMS error) compared to Gaussian Random Projections.
*   **Dynamic Analysis:** Visual reconstructions of 2D manifolds (spirals and circles) mapped to high-dimensional latent spaces and projected back, demonstrating the invertibility of the transform.

---

## 📝 Citation

If you use this code or concepts in your research, please cite our paper:

```bibtex
@article{primal2025,
  title={Primal: A Unified Deterministic Framework for Quasi-Orthogonal Hashing and Manifold Learning},
  author={Vladimer Khasia},
  journal={arXiv},
  year={2025}
}
```

---

*For questions or issues, please open an issue in this repository.*