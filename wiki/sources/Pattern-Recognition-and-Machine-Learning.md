---
type: source
title: "Pattern Recognition and Machine Learning"
address: c-000003
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - machine-learning
  - pattern-recognition
  - bayesian
  - textbook
status: current
source_url: https://www.microsoft.com/en-us/research/wp-content/uploads/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf
raw_file: ".raw/articles/pattern-recognition-and-machine-learning-2006-06-28.md"
related:
  - "[[Christopher Bishop]]"
  - "[[Microsoft Research]]"
  - "[[Springer]]"
  - "[[Bayesian Methods]]"
  - "[[Graphical Models]]"
  - "[[Approximate Inference]]"
  - "[[Kernel Methods]]"
---

# Source: Pattern Recognition and Machine Learning

**Author**: [[Christopher Bishop]] (F.R.Eng., then Assistant Director, [[Microsoft Research]] Ltd, Cambridge, U.K.)
**Publisher**: [[Springer]] Science+Business Media, 2006 — *Information Science and Statistics* series (eds. M. Jordan, J. Kleinberg, B. Schölkopf)
**ISBN**: 978-0387-31073-2 · **Length**: ~738 pages

> [!key-insight] Why this book matters
> "PRML" is one of the canonical graduate-level introductions to machine learning, distinctive for treating the field through a **Bayesian, probabilistic** lens rather than as a catalogue of algorithms. Its framing — Bayesian methods, graphical models, approximate inference, and kernels as the four pillars — shaped how a generation learned the subject.

## What it covers

A comprehensive, self-contained introduction to pattern recognition and machine learning aimed at advanced undergraduates / first-year PhD students. Assumes multivariate calculus and linear algebra; builds probability from scratch. Every chapter ends with graded exercises (⋆–⋆⋆⋆).

### Chapter structure (14 chapters)

| # | Chapter | Theme |
|---|---------|-------|
| 1 | Introduction | Curve fitting, over-fitting, bias–variance, decision theory, information theory |
| 2 | Probability Distributions | Exponential family, conjugate priors, nonparametric density |
| 3 | Linear Models for Regression | Basis functions, bias–variance, [[Bayesian Methods\|Bayesian]] linear regression |
| 4 | Linear Models for Classification | Discriminants, logistic regression, Laplace approximation |
| 5 | Neural Networks | Multilayer perceptrons, backprop, regularization, Bayesian nets |
| 6 | [[Kernel Methods]] | Dual representations, Gaussian processes |
| 7 | Sparse [[Kernel Methods\|Kernel]] Machines | Support vector machines, RVMs |
| 8 | [[Graphical Models]] | Bayesian networks, Markov random fields, inference on graphs |
| 9 | Mixture Models and EM | K-means, Gaussian mixtures, expectation–maximization |
| 10 | [[Approximate Inference]] | Variational Bayes, expectation propagation |
| 11 | Sampling Methods | MCMC, Gibbs, Metropolis–Hastings |
| 12 | Continuous Latent Variables | PCA, probabilistic PCA, factor analysis |
| 13 | Sequential Data | HMMs, linear dynamical systems |
| 14 | Combining Models | Committees, boosting, mixtures of experts |

## The four pillars (from the preface)

The author frames the book's distinctive contribution around four developments of the prior decade:

1. **[[Bayesian Methods]]** — moved "from a specialist niche to mainstream."
2. **[[Graphical Models]]** — "a general framework for describing and applying probabilistic models."
3. **[[Approximate Inference]]** — variational Bayes and expectation propagation made Bayesian methods practical.
4. **[[Kernel Methods]]** — "significant impact on both algorithms and applications."

## Pedagogical entry point

Chapter 1 opens with **polynomial curve fitting** (fitting noisy samples of sin(2πx)) to motivate generalization, over-fitting, the bias–variance trade-off, and a Bayesian treatment of model complexity — recurring themes throughout.

## Relation to this vault

This is a reference source ingested as a demonstration of the [[LLM Wiki Pattern]] ingest pipeline. It is topically independent of the claude-obsidian ecosystem; see [[log]] for the ingest record.

## See also

- [[Christopher Bishop]] · [[Microsoft Research]] · [[Springer]]
- [[Bayesian Methods]] · [[Graphical Models]] · [[Approximate Inference]] · [[Kernel Methods]]
