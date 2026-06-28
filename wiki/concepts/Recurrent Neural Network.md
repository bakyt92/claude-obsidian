---
type: concept
title: "Recurrent Neural Network"
address: c-000026
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - deep-learning
  - sequence-modeling
status: developing
related:
  - "[[Deep Learning (Goodfellow, Bengio, Courville)]]"
  - "[[Self-Attention]]"
  - "[[Transformer]]"
  - "[[Backpropagation]]"
---

# Recurrent Neural Network

An **RNN** processes a sequence one step at a time, carrying a **hidden state** that summarizes everything seen so far. The same weights are applied at every timestep (parameter sharing across time), so the network can handle variable-length input. It was the dominant approach to sequence modeling before the [[Transformer]].

> [!key-insight] Memory through a loop
> Unfold the recurrence and an RNN becomes a very deep feedforward net — one layer per timestep — trained by **backpropagation through time** (BPTT, a [[Backpropagation]] variant). That depth is also its weakness: gradients vanish or explode over long sequences, so plain RNNs struggle with **long-term dependencies**. [[Deep Learning (Goodfellow, Bengio, Courville)]] Ch 10 develops RNNs, bidirectional/encoder-decoder variants, and the gated fixes.

## Gated variants

- **LSTM** (Long Short-Term Memory) and **GRU** add gates that let the network *keep* or *forget* information selectively, largely solving the vanishing-gradient problem for moderate ranges.
- Encoder–decoder (seq2seq) RNNs powered early neural machine translation.

## Why it matters here — the bridge to attention

> [!gap] What RNNs couldn't do, attention did
> RNNs are **inherently sequential**: timestep `t` needs timestep `t-1`, so they don't parallelize across positions and still strain on very long dependencies. [[Self-Attention]] removed the recurrence entirely — every position attends to every other in one parallel matrix operation — which is why the [[Transformer]] (2017) displaced RNNs for most NLP. [[Deep Learning (Goodfellow, Bengio, Courville)]] (2016) predates this shift, so it presents RNN/LSTM as the state of the art for sequences. Reading it alongside [[Modern Large Language Models]] shows the before/after of the attention revolution.
