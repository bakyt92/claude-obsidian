---
type: source
title: "Data Science from Scratch"
address: c-000009
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - data-science
  - machine-learning
  - python
  - textbook
status: current
source_url: https://github.com/Benlau93/Data-Science-Curriculum/blob/master/Data%20Science%20from%20Scratch-%20First%20Principles%20with%20Python.pdf
raw_file: ".raw/articles/data-science-from-scratch-2026-06-28.md"
pdf_file: ".raw/pdfs/data-science-from-scratch.pdf"
related:
  - "[[Joel Grus]]"
  - "[[O'Reilly Media]]"
  - "[[From-Scratch Pedagogy]]"
  - "[[Linear Algebra]]"
  - "[[Pattern Recognition and Machine Learning]]"
  - "[[DSFS vs PRML]]"
---

# Source: Data Science from Scratch

**Author**: [[Joel Grus]]
**Publisher**: [[O'Reilly Media]], April 2015 (1st Edition)
**ISBN**: 978-1-491-90142-7 · 330 pages · Python 2.7
**Subtitle**: *First Principles with Python*

> [!key-insight] The thesis
> Libraries (NumPy, pandas, scikit-learn) let you *do* data science without *understanding* it. This book teaches the opposite way: **implement every fundamental algorithm by hand, in pure Python**, so the mechanics are visible. It is the canonical worked example of [[From-Scratch Pedagogy]]. Where [[Pattern Recognition and Machine Learning]] gives the rigorous Bayesian theory, DSFS gives the runnable, hackable intuition — see [[DSFS vs PRML]].

## What it covers

Data science as the intersection of **hacking skills + math/statistics**. The book walks bottom-up from Python and visualization through the math foundations, then implements a standard ML curriculum from scratch.

| Block | Chapters | Topics |
|-------|----------|--------|
| Tooling | 1–3 | intro, Python crash course, visualizing data (matplotlib) |
| Math foundations | 4–8 | [[Linear Algebra]] (vectors/matrices by hand), statistics, probability, hypothesis & inference, **gradient descent** |
| Data wrangling | 9–10 | getting data (scraping, APIs), cleaning/munging, rescaling, dimensionality reduction |
| ML core | 11–19 | the ML frame (overfitting, bias-variance), k-NN, Naive Bayes, linear & multiple regression, logistic regression + SVMs, decision trees, **neural networks**, clustering |
| Applications | 20–24 | NLP (topic modeling, Gibbs sampling), network analysis (PageRank), recommender systems, databases & SQL, MapReduce |
| Wrap | 25 | "Go forth": IPython, NumPy, pandas, scikit-learn, where to go next |

## Why it matters to this vault

- It is the **applied complement** to [[Pattern Recognition and Machine Learning]]: same ML territory, opposite altitude (code-first vs. theory-first).
- Chapter 4 builds [[Linear Algebra]] (vectors and matrices) from scratch in Python — a concrete instance of the [[Four Fundamental Subspaces]] / matrix machinery the math pages describe.
- Its "build it to understand it" ethos rhymes with this vault's own source-first, synthesize-don't-import discipline (see [[Source-First Synthesis]]).

## Notable

- Recurring narrative device: **"DataSciencester,"** a fictional social network for data scientists, used as the running dataset.
- [[Joel Grus]] is also widely known for the talk *"I Don't Like Notebooks."*
- A revised **2nd edition (2019)** ports everything to Python 3.6; this source is the 1st edition (Python 2.7).
