---
type: source
title: "MIT 18.06 Linear Algebra"
address: c-000004
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - linear-algebra
  - mathematics
  - course
  - mit
status: current
source_url: https://web.mit.edu/18.06/www/
raw_file: ".raw/articles/mit-18.06-linear-algebra-2026-06-28.md"
related:
  - "[[Gilbert Strang]]"
  - "[[MIT OpenCourseWare]]"
  - "[[Linear Algebra]]"
  - "[[Four Fundamental Subspaces]]"
  - "[[Pattern Recognition and Machine Learning]]"
---

# Source: MIT 18.06 Linear Algebra

**Instructor**: [[Gilbert Strang]] (Professor of Mathematics, MIT)
**Host**: MIT Mathematics Department · archived on [[MIT OpenCourseWare]]
**URL**: https://web.mit.edu/18.06/www/

> [!key-insight] Why this source matters
> 18.06 is arguably the most widely-watched linear algebra course in the world. Strang's lecture videos (Spring 2005, 34 lectures on YouTube/OCW) and his "[[Four Fundamental Subspaces]]" framing reshaped how the subject is taught — leading with the *geometry* and *subspace structure* of `Ax = b` rather than abstract axioms. It supplies exactly the [[Linear Algebra]] background that texts like [[Pattern Recognition and Machine Learning]] assume but do not teach.

## What it is

The course home page acts as a hub linking the live materials and the archive:

- **Current semester** — GitHub repo `mitmath/1806` (problem sets, exams, Julia notebooks).
- **OpenCourseWare** — Spring 2010 archived run with full video.
- **Video lectures** — the canonical 34-lecture Spring 2005 series.
- **Archive** — past problem sets and exams *with solutions*.
- **Julia** — computational examples for numerical experiments.

## Curriculum arc (34 lectures)

| Block | Topics |
|-------|--------|
| Solving `Ax = b` | geometry of equations, elimination, matrix multiplication, **LU** factorization, transposes, permutations |
| Vector spaces | column space & nullspace, `Ax = 0` / `Ax = b`, independence, **basis & dimension**, [[Four Fundamental Subspaces]] |
| Orthogonality | projections, **least squares**, orthogonal matrices, **Gram–Schmidt** (`A = QR`) |
| Determinants | properties, cofactors, Cramer's rule, inverse, volume |
| Eigenvalues | eigenvectors, **diagonalization** `A = SΛS⁻¹`, powers `Aⁿ`, differential equations & `exp(At)`, **Markov matrices** |
| Special structure | symmetric & **positive-definite** matrices, complex matrices, the **FFT**, similar matrices & **Jordan form**, the **SVD** |
| Transformations | linear transformations, change of basis, left/right/pseudo inverses |

See the [[Linear Algebra]] concept page for how these pieces fit together.

## Assessment

Three in-term quizzes (each with a review lecture) plus a final exam. Past quizzes and the final are posted with solutions.

## Connections

- [[Gilbert Strang]] is also the author of the *Introduction to Linear Algebra* textbook the course tracks.
- The SVD / eigenvalue / projection machinery here (see [[Linear Algebra]]) is the prerequisite that [[Pattern Recognition and Machine Learning]] leans on for PCA, least squares, and kernel methods.
