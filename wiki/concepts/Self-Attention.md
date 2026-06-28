---
type: concept
title: "Self-Attention"
address: c-000018
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - llm
  - deep-learning
  - attention
status: developing
related:
  - "[[Transformer]]"
  - "[[Modern Large Language Models]]"
  - "[[Linear Algebra]]"
  - "[[Recurrent Neural Network]]"
---

# Self-Attention

The mechanism at the heart of the [[Transformer]]: each token decides **how much to attend to every other token** in the sequence, and builds its new representation as a weighted blend of their values.

> [!key-insight] Query, Key, Value
> Every token is projected into three vectors: a **Query** (what am I looking for?), a **Key** (what do I offer?), and a **Value** (what do I pass on?). The attention score between two tokens is the **scaled dot product** of one's Query with the other's Key; a **softmax** turns the scores for a given token into weights that sum to 1; the output is the weighted sum of all Values. [[Modern Large Language Models]] walks this through concretely on a 6-token sequence (Ch 5).

## Key properties

- **Scores vs. weights**: raw dot-product scores become weights only after softmax (and scaling by `1/√d_k` for numerical stability).
- **Multi-head**: run several attention computations in parallel on different learned projections, then concatenate — lets the model attend to different relationships at once.
- **Parallelizable**: all pairwise scores are one big matrix multiply `QKᵀ`, so the whole layer is GPU-friendly (the property that killed the RNN).
- **Causal masking**: in a GPT decoder, a mask prevents a token from attending to future positions, so training matches autoregressive generation.

## Cost and modern variants

Naive self-attention is **O(n²)** in sequence length. [[Modern Large Language Models]] (Ch 17) covers the efficiency lineage: FlashAttention (IO-aware exact attention), grouped/multi-query attention (GQA/MQA, fewer K/V heads), KV caching for fast inference, and recurrent Mamba-style alternatives.

Attention's rise is best understood against what it replaced: the sequential [[Recurrent Neural Network]] (RNN/LSTM), which couldn't parallelize across positions and strained on long-range dependencies. Self-attention removed the recurrence entirely.

## Grounding

Pure [[Linear Algebra]]: Q, K, V are linear projections; the score matrix is `QKᵀ`; the output is `softmax(QKᵀ/√d)·V`. Implemented line-by-line in [[PyTorch]] in the source (Ch 8).
