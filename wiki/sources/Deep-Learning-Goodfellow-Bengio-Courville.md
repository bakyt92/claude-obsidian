---
type: source
title: "Deep Learning (Goodfellow, Bengio, Courville)"
address: c-000020
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - deep-learning
  - machine-learning
  - textbook
  - foundational
status: current
source_url: https://aikosh.indiaai.gov.in/static/Deep+Learning+Ian+Goodfellow.pdf
original_file: ".raw/pdfs/deep-learning-goodfellow.pdf"
raw_file: ".raw/articles/deep-learning-goodfellow-2026-06-28.md"
related:
  - "[[Ian Goodfellow]]"
  - "[[Yoshua Bengio]]"
  - "[[MIT Press]]"
  - "[[Backpropagation]]"
  - "[[Generative Adversarial Network]]"
  - "[[Recurrent Neural Network]]"
  - "[[Linear Algebra]]"
  - "[[Pattern Recognition and Machine Learning]]"
  - "[[Modern Large Language Models]]"
---

# Source: Deep Learning (Goodfellow, Bengio, Courville)

**Authors**: [[Ian Goodfellow]], [[Yoshua Bengio]], Aaron Courville
**Publisher**: [[MIT Press]], 2016 · ~800 pages · companion site `www.deeplearningbook.org`

> [!key-insight] The foundational text
> "The Goodfellow book" is *the* canonical graduate reference for deep learning. It is theory- and math-first: it builds the mathematical foundations, then modern practical networks, then a research survey. Where [[Modern Large Language Models]] teaches by building, and [[Data Science from Scratch]] teaches classical ML by coding, this book teaches the **mathematics and principles** of deep nets — closest in register to [[Pattern Recognition and Machine Learning]].

## Structure (20 chapters, 3 parts)

| Part | Chapters | Focus |
|------|----------|-------|
| I — Math & ML basics | 2–5 | [[Linear Algebra]] (SVD, eigendecomposition, PCA), probability & information theory, numerical computation, ML basics (bias-variance, MLE, capacity) |
| II — Practical deep nets | 6–12 | feedforward nets & [[Backpropagation]]; regularization (dropout); optimization (SGD, Adam); convolutional networks; [[Recurrent Neural Network|RNNs/LSTMs]]; methodology; applications (vision, speech, NLP) |
| III — Research | 13–20 | linear factor models, autoencoders, representation learning, structured probabilistic models, Monte Carlo, partition function, approximate inference (variational), **deep generative models** incl. [[Generative Adversarial Network|GANs]] |

## Why it matters to this vault

- **The theoretical bedrock** under everything else in the AI cluster. The training math ([[Backpropagation]], SGD), the architectures, and the generative models here are the foundation that [[Modern Large Language Models]] builds on practically.
- **Math grounding** is explicit: Chapter 2 is a self-contained [[Linear Algebra]] primer (SVD, eigendecomposition, pseudoinverse, PCA) — the same machinery the [[Linear Algebra]] concept page describes, applied to deep nets.
- **Register twin of [[Pattern Recognition and Machine Learning]]**: both rigorous, math-first graduate texts. PRML (2006) is Bayesian/classical ML; this (2016) is deep nets. Together they bracket the pre-deep and deep eras.

> [!gap] Predates the Transformer
> Published 2016, this book covers sequence modeling via [[Recurrent Neural Network|RNNs and LSTMs]] — it does **not** cover self-attention or transformers ("Attention Is All You Need" came in 2017). For that architecture see [[Transformer]] / [[Self-Attention]] and [[Modern Large Language Models]]. This is a clean historical boundary, not a contradiction: the book is foundational but pre-attention.

## Provenance

A clean PDF (801 pp) mirrored on India's AIKosh (IndiaAI) static host; matches the well-known MIT Press edition. Free HTML is also at the official `deeplearningbook.org`.
