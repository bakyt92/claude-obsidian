---
type: concept
title: "Linear Algebra"
address: c-000007
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - mathematics
  - linear-algebra
status: developing
related:
  - "[[MIT 18.06 Linear Algebra]]"
  - "[[Gilbert Strang]]"
  - "[[Four Fundamental Subspaces]]"
  - "[[Pattern Recognition and Machine Learning]]"
---

# Linear Algebra

The mathematics of **vectors, vector spaces, and linear maps** — concretely, the study of systems `Ax = b` and the structure of the matrix `A`. It is the computational substrate of nearly all modern machine learning, graphics, optimization, and scientific computing.

> [!key-insight] Strang's organizing idea
> Treat a matrix as a *map between subspaces*, not a grid of numbers. Almost every 18.06 topic is a different lens on the same object `A`: how it acts on its [[Four Fundamental Subspaces]], and how it can be **factored** to expose that action.

## The big factorizations

Most of [[MIT 18.06 Linear Algebra]] can be read as a tour of decompositions, each isolating one aspect of `A`:

| Factorization | Reveals |
|---------------|---------|
| `A = LU` | Gaussian elimination / solving `Ax = b` |
| `A = QR` | orthonormal basis via Gram–Schmidt; least squares |
| `A = SΛS⁻¹` | eigenvalues — behavior of powers `Aⁿ`, `exp(At)` |
| `A = QΛQᵀ` | spectral theorem for symmetric / positive-definite `A` |
| `A = UΣVᵀ` | the **SVD** — the universal factorization, works for any matrix |

## Why it matters to ML

[[Pattern Recognition and Machine Learning]] explicitly *assumes* linear algebra and builds on it: PCA is an eigen/SVD problem, linear regression is least squares (projection onto the column space), and kernel methods live in inner-product spaces. 18.06 supplies exactly this background. For a hands-on counterpart, [[Data Science from Scratch]] (Chapter 4) implements vectors and matrices from scratch in Python rather than assuming them. [[Deep Learning (Goodfellow, Bengio, Courville)]] devotes its Chapter 2 to exactly this linear-algebra primer (SVD, eigendecomposition, pseudoinverse, PCA) as the foundation for deep nets.

## Core threads (see the course for full treatment)

- **Solving systems**: elimination, pivots, free vs. pivot variables, complete solution to `Ax = b`.
- **Subspace structure**: the [[Four Fundamental Subspaces]], rank, basis, dimension, independence.
- **Orthogonality**: projections, least squares, orthonormal bases, Gram–Schmidt.
- **Eigentheory**: eigenvalues/eigenvectors, diagonalization, symmetric & positive-definite matrices, the SVD.
- **Applications**: differential equations, Markov matrices, networks/graphs, the FFT.
