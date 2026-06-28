---
type: concept
title: "Backpropagation"
address: c-000024
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - deep-learning
  - optimization
  - training
status: developing
related:
  - "[[Deep Learning (Goodfellow, Bengio, Courville)]]"
  - "[[Transformer]]"
  - "[[Linear Algebra]]"
  - "[[PyTorch]]"
---

# Backpropagation

The algorithm that computes the **gradient of a neural network's loss with respect to every parameter**, by applying the chain rule backwards through the network's computational graph. It is what makes gradient-based training of deep nets feasible — and therefore the engine under essentially every model in this vault's AI cluster.

> [!key-insight] Chain rule on a graph
> A network is a composition of functions. The **forward pass** computes the output and loss. The **backward pass** walks the computational graph in reverse, multiplying local derivatives (the chain rule) to get `∂loss/∂each-weight` in one efficient sweep — reusing intermediate results instead of recomputing them. Those gradients then feed an optimizer (SGD, Adam) that nudges the weights downhill. [[Deep Learning (Goodfellow, Bengio, Courville)]] develops this in Ch 6.5 ("Back-Propagation and Other Differentiation Algorithms").

## Key points

- **Not learning itself** — backprop only computes gradients; the optimizer (gradient descent and variants) does the updating.
- **Reverse-mode autodiff**: backprop is the deep-learning name for reverse-mode automatic differentiation, which frameworks like [[PyTorch]] implement generically (`autograd`).
- **Why it scales**: cost is roughly the same order as the forward pass, regardless of the number of parameters — the property that lets billion-parameter models train at all.

## Connections in this vault

- It is how the [[Transformer]] and [[Self-Attention]] layers in [[Modern Large Language Models]] are trained — Q/K/V projections, attention weights, and FFN weights all get gradients via backprop.
- Built on [[Linear Algebra]] and calculus: gradients are vectors/Jacobians; the backward pass is chained matrix products.
- The "gradient-based optimization" foundations sit in [[Deep Learning (Goodfellow, Bengio, Courville)]] Ch 4 and Ch 8.
