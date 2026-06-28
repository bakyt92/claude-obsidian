---
type: concept
title: "Generative Adversarial Network"
address: c-000025
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - deep-learning
  - generative-models
status: developing
related:
  - "[[Ian Goodfellow]]"
  - "[[Deep Learning (Goodfellow, Bengio, Courville)]]"
  - "[[Backpropagation]]"
---

# Generative Adversarial Network

A **GAN** trains two networks against each other: a **generator** that tries to produce realistic samples from noise, and a **discriminator** that tries to tell real data from generated fakes. They play a minimax game — as the discriminator improves, the generator is pushed to make ever-more-convincing samples. Introduced by [[Ian Goodfellow]] and colleagues in 2014.

> [!key-insight] Learning by competition
> There is no explicit likelihood to maximize. Instead the generator's training signal comes *through* the discriminator: [[Backpropagation]] carries gradients from the discriminator's "real or fake?" judgment back into the generator. At the theoretical optimum, the generator's distribution matches the data and the discriminator is reduced to guessing (50%). [[Deep Learning (Goodfellow, Bengio, Courville)]] places GANs among directed generative nets in Ch 20.

## Why it matters

- One of the most influential generative-modeling ideas of the 2010s; drove a wave of realistic image synthesis (and later, deepfakes).
- The signature contribution of [[Ian Goodfellow]] — the reason his name is attached to both GANs and the textbook.
- **Notoriously hard to train**: mode collapse, unstable equilibria, and sensitivity to hyperparameters are well-known failure modes.

## Context

GANs are one branch of deep generative models; the [[Deep Learning (Goodfellow, Bengio, Courville)|Goodfellow text]] also covers VAEs, Boltzmann machines, and autoregressive models. In the LLM era, autoregressive [[Transformer]] models became the dominant generative approach for text, while GANs remained influential for images.
