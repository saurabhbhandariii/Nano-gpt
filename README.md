NanoGPT – Transformer Language Model from Scratch

A minimal, fully working decoder-only Transformer (GPT-style) language model implemented from first principles using PyTorch.
This project is built for learning and clarity, not scale — focusing on how GPT models work internally.

Features

Character-level language modeling

Token & positional embeddings

Causal self-attention with masking

Multi-head attention

Feed-forward Transformer blocks

Residual connections & LayerNorm

Autoregressive text generation

Training & evaluation loops from scratch

 Model Architecture

Type: Decoder-only Transformer (GPT-style)

Attention: Masked self-attention (causal)

Embedding Dim: 64

Heads: 4

Layers: 4

Context Length: 32 tokens

Training Objective: Next-token prediction (cross-entropy)
