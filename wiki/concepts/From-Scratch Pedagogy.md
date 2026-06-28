---
type: concept
title: "From-Scratch Pedagogy"
address: c-000012
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - pedagogy
  - learning
  - data-science
status: developing
related:
  - "[[Data Science from Scratch]]"
  - "[[Joel Grus]]"
  - "[[Source-First Synthesis]]"
  - "[[Pattern Recognition and Machine Learning]]"
  - "[[Modern Large Language Models]]"
---

# From-Scratch Pedagogy

The teaching philosophy that you understand a tool only after **building it by hand** — implementing an algorithm in plain code before reaching for a library that hides it. [[Joel Grus]]'s [[Data Science from Scratch]] is the canonical worked example: it implements vectors, gradient descent, k-NN, regression, decision trees, and neural networks in pure Python rather than calling NumPy or scikit-learn.

> [!key-insight] Why "from scratch" works
> Libraries optimize for *doing*; from-scratch implementation optimizes for *understanding*. Re-deriving an algorithm forces you to confront every assumption (numerical stability, edge cases, the actual math) that a one-line library call papers over. The cost is performance and production-readiness — which is exactly why the book ends ([[Data Science from Scratch|Chapter 25]]) by pointing you back to NumPy/pandas/scikit-learn for real work.

## The trade

| | From scratch | Library-first |
|---|---|---|
| Goal | understanding mechanics | shipping results |
| Speed to result | slow | fast |
| Depth of intuition | high | low |
| Production fit | poor (toy code) | strong |

## Connections in this vault

- Contrast with [[Pattern Recognition and Machine Learning]], which builds understanding through **mathematical derivation** rather than code — a different "from first principles" route to the same goal. See [[DSFS vs PRML]].
- [[Modern Large Language Models]] applies the same ethos one ML-generation later: build a GPT-mini from scratch in [[PyTorch]] to understand transformers, rather than calling a model API.
- Rhymes with this vault's [[Source-First Synthesis]]: don't import a pre-chewed summary; read the primary source and synthesize it yourself. Same instinct, applied to knowledge work instead of algorithms.
- **The counterpoint**: [[Data Science for Beginners]] (Microsoft) deliberately teaches *library-first* (Pandas, Matplotlib, even low-code Azure ML). It optimizes for shipping results over understanding internals — the live tradeoff this concept names. Neither is "right"; they suit different learners and goals.
