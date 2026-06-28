---
type: concept
title: "Four Fundamental Subspaces"
address: c-000008
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - mathematics
  - linear-algebra
status: developing
related:
  - "[[Linear Algebra]]"
  - "[[MIT 18.06 Linear Algebra]]"
  - "[[Gilbert Strang]]"
---

# Four Fundamental Subspaces

[[Gilbert Strang]]'s signature framing of [[Linear Algebra]]: every `m × n` matrix `A` defines **four** subspaces whose dimensions and orthogonality relationships capture everything about how `A` acts.

| Subspace | Lives in | Dimension |
|----------|----------|-----------|
| **Column space** `C(A)` | ℝᵐ | rank `r` |
| **Nullspace** `N(A)` | ℝⁿ | `n − r` |
| **Row space** `C(Aᵀ)` | ℝⁿ | rank `r` |
| **Left nullspace** `N(Aᵀ)` | ℝᵐ | `m − r` |

> [!key-insight] The orthogonality picture
> Within ℝⁿ, the **row space and nullspace are orthogonal complements**. Within ℝᵐ, the **column space and left nullspace are orthogonal complements**. `A` maps the row space *one-to-one onto* the column space; everything in the nullspace collapses to zero. This is the geometric heart of the intuition for `Ax = b`.

## Why it's the centerpiece

- **Solvability of `Ax = b`**: solvable exactly when `b` lies in `C(A)`.
- **Uniqueness**: the solution is unique iff `N(A) = {0}` (full column rank).
- **Least squares**: projecting `b` onto `C(A)` is what regression does when `b ∉ C(A)`.
- It makes **rank** the single most important number about a matrix: it fixes all four dimensions at once.

Strang calls the relationships among these four spaces "the big picture of linear algebra" — it is the lens [[MIT 18.06 Linear Algebra]] returns to throughout.
