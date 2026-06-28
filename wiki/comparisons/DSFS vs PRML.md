---
type: comparison
title: "DSFS vs PRML"
address: c-000013
created: 2026-06-28
updated: 2026-06-28
tags:
  - comparison
  - machine-learning
  - data-science
  - textbook
status: developing
related:
  - "[[Data Science from Scratch]]"
  - "[[Pattern Recognition and Machine Learning]]"
  - "[[From-Scratch Pedagogy]]"
---

# Data Science from Scratch vs. Pattern Recognition and Machine Learning

Two ML texts now in the vault that cover overlapping territory from **opposite altitudes**. This page is a chooser, not a ranking.

| Dimension | [[Data Science from Scratch]] (Grus, 2015) | [[Pattern Recognition and Machine Learning]] (Bishop, 2006) |
|-----------|--------------------------------------------|-------------------------------------------------------------|
| Register | practitioner / hacker | graduate academic |
| Method | implement in pure Python ([[From-Scratch Pedagogy]]) | derive the mathematics |
| Math depth | intuition + "cartoon" math | full Bayesian, probabilistic rigor |
| Prereqs | some Python + light math | multivariate calculus + [[Linear Algebra]] |
| Length | 330 pp | ~738 pp |
| Publisher | [[O'Reilly Media]] | [[Springer]] |
| Best for | "show me the code; I learn by building" | "show me the theory; I want to know *why* it's correct" |

> [!key-insight] They are complements, not substitutes
> Read **DSFS first** to build runnable intuition for k-NN, regression, gradient descent, and neural nets; reach for **PRML** when you need the probabilistic foundations (priors, marginalization, graphical models, the bias-variance decomposition done properly). DSFS shows you *that* an algorithm works; PRML shows you *why*.

## Overlap map

Both cover: linear & logistic regression, neural networks, clustering, Naive Bayes, dimensionality reduction. PRML adds depth on kernels, graphical models, and approximate inference that DSFS only gestures at. DSFS adds practical plumbing (scraping data, SQL, MapReduce, visualization) that PRML, a pure theory text, omits entirely.

## See also

- [[From-Scratch Pedagogy]] — the learning philosophy DSFS embodies.
- [[Wiki vs RAG]] — another "when to use which" comparison in this vault.
