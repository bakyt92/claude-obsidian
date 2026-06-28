---
type: entity
title: "PyTorch"
address: c-000016
created: 2026-06-28
updated: 2026-06-28
tags:
  - entity
  - product
  - framework
  - deep-learning
status: developing
related:
  - "[[Modern Large Language Models]]"
  - "[[Transformer]]"
  - "[[Self-Attention]]"
---

# PyTorch

**What**: Open-source deep-learning framework, originally from Meta AI (now under the PyTorch Foundation / Linux Foundation). Provides tensors with GPU acceleration and reverse-mode automatic differentiation (autograd), plus the `torch.nn` building blocks for neural networks.

In this vault, PyTorch is the implementation substrate of [[Modern Large Language Models]]: the book codes [[Self-Attention]], the [[Transformer]] block, and a full "GPT-mini" from scratch in pure PyTorch, with appendices on autograd, gradient checking, and hardware recipes (CPU/GPU/Colab/cloud).

## Why it matters here

- It is the **how** behind the book's [[From-Scratch Pedagogy]]: low-level enough to expose the math (manual Q/K/V, attention masks, backprop), high-level enough to actually train a model.
- The de facto standard for LLM research and from-scratch teaching (cf. Karpathy's nanoGPT, also PyTorch). See [[Andrej Karpathy]].
