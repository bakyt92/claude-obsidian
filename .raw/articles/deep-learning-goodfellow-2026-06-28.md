---
source_url: https://aikosh.indiaai.gov.in/static/Deep+Learning+Ian+Goodfellow.pdf
pdf_file: .raw/pdfs/deep-learning-goodfellow.pdf
fetched: 2026-06-28
extraction: pypdf (front matter + ToC); 801 pages
md5: 62844ffb883bb23d81b9303703c0eb27
---

# Deep Learning

**Authors**: Ian Goodfellow, Yoshua Bengio, Aaron Courville
**Publisher**: MIT Press, 2016 · ~800 pages · companion site www.deeplearningbook.org
**Note**: written largely while Goodfellow was at Google Brain; thanks Geoffrey Hinton, Samy Bengio, Greg Corrado.

## Premise

The first comprehensive textbook on deep learning. Builds the mathematical
foundations (linear algebra, probability, numerical computation, ML basics), then
the modern practical networks (feedforward, regularization, optimization, CNNs,
RNNs), then a research-level survey (representation learning, structured
probabilistic models, Monte Carlo methods, approximate inference, deep generative
models). Theory- and math-first, not a code/from-scratch tutorial.

> Important historical note: published 2016, this book PRE-DATES the Transformer
> ("Attention Is All You Need," 2017). Sequence modeling here is RNN/LSTM-centric;
> self-attention and transformers are NOT covered.

## Table of Contents (20 chapters, 3 parts)

1. Introduction (who should read; historical trends in deep learning)

### Part I — Applied Math and Machine Learning Basics
2. Linear Algebra (vectors/matrices/tensors, norms, eigendecomposition, SVD, Moore-Penrose pseudoinverse, trace, determinant, PCA)
3. Probability and Information Theory (random variables, distributions, Bayes' rule, information theory, structured probabilistic models)
4. Numerical Computation (overflow/underflow, conditioning, gradient-based optimization, constrained optimization)
5. Machine Learning Basics (learning algorithms, capacity/overfitting/underfitting, hyperparameters, bias-variance, MLE, Bayesian statistics, supervised & unsupervised algorithms, SGD, building an ML algorithm, curse of dimensionality)

### Part II — Modern Practical Deep Networks
6. Deep Feedforward Networks (gradient learning, hidden units, architecture design, **back-propagation**)
7. Regularization for Deep Learning (parameter norm penalties, dataset augmentation, early stopping, **dropout**, adversarial training)
8. Optimization for Training Deep Models (how learning differs from pure optimization, challenges, basic algorithms, adaptive learning rates, second-order methods)
9. Convolutional Networks (the convolution operation, pooling, variants, the neuroscientific basis, history)
10. Sequence Modeling: Recurrent and Recursive Nets (unfolding graphs, **RNNs**, bidirectional/encoder-decoder, **LSTM** and gated RNNs, long-term dependencies, explicit memory)
11. Practical Methodology (performance metrics, baselines, hyperparameter selection, debugging)
12. Applications (large-scale DL, computer vision, speech recognition, NLP, other)

### Part III — Deep Learning Research
13. Linear Factor Models
14. Autoencoders (undercomplete, regularized, denoising, contractive, manifold learning)
15. Representation Learning (greedy layer-wise pretraining, transfer learning, distributed representation, exponential gains from depth)
16. Structured Probabilistic Models for Deep Learning (graphs to describe model structure)
17. Monte Carlo Methods (sampling, importance sampling, MCMC, Gibbs)
18. Confronting the Partition Function (pseudolikelihood, score matching, noise-contrastive estimation)
19. Approximate Inference (inference as optimization, EM, MAP/sparse coding, variational inference)
20. Deep Generative Models (Boltzmann machines, RBMs, deep belief nets, deep Boltzmann machines, back-prop through random operations, directed generative nets incl. **GANs**/VAEs, generative stochastic networks, evaluating generative models)
