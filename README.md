# NanoGPT – Transformer Language Model from Scratch

A minimal implementation of a **decoder-only Transformer (GPT-style)** language model built **from first principles** using PyTorch.  
This project focuses on understanding the **core internals of GPT models** rather than scale or production optimizations.

---

## Overview

This project implements a small-scale GPT model trained using **autoregressive next-token prediction**.  
All major Transformer components are implemented manually without relying on high-level LLM frameworks.

The model is trained on a character-level text dataset (Tiny Shakespeare) and can generate coherent text sequences.

---

## Model Architecture

- Decoder-only Transformer (GPT-style)
- Token Embeddings + Positional Embeddings
- Masked (causal) Self-Attention
- Multi-Head Attention
- Feed-Forward Networks (MLP)
- Residual Connections
- Layer Normalization
- Cross-Entropy Loss for next-token prediction

---

## Hyperparameters

- Embedding Dimension: 64  
- Number of Heads: 4  
- Number of Transformer Layers: 4  
- Context Length (Block Size): 32  
- Optimizer: AdamW  
- Learning Rate: 1e-3  

---

## Dataset

The model is trained on **Tiny Shakespeare**, a small character-level dataset.

You can download it using:

```bash
wget https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt
