NanoGPT – Transformer Language Model from Scratch

A minimal, fully working decoder-only Transformer (GPT-style) language model implemented from first principles using PyTorch.
This project is built for learning and clarity, not scale — focusing on how GPT models work internally.

🚀 Features

Character-level language modeling

Token & positional embeddings

Causal self-attention with masking

Multi-head attention

Feed-forward Transformer blocks

Residual connections & LayerNorm

Autoregressive text generation

Training & evaluation loops from scratch

🧠 Model Architecture

Type: Decoder-only Transformer (GPT-style)

Attention: Masked self-attention (causal)

Embedding Dim: 64

Heads: 4

Layers: 4

Context Length: 32 tokens

Training Objective: Next-token prediction (cross-entropy)

📁 Project Structure
.
├── input.txt          # Training text (e.g. Tiny Shakespeare)
├── model.py           # NanoGPT implementation
├── train.py           # Training loop & evaluation
├── README.md


Note: The project can also be run as a single script if preferred.

⚙️ Setup & Installation
1. Clone the repository
git clone https://github.com/your-username/nanogpt-from-scratch.git
cd nanogpt-from-scratch

2. Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

3. Install dependencies
pip install torch

📊 Dataset

This project uses Tiny Shakespeare, a small character-level text dataset.

wget https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt


You can replace input.txt with any plain-text dataset.

🏋️ Training the Model

Run:

python train.py


During training, the script:

Samples mini-batches

Computes cross-entropy loss

Evaluates train/validation loss periodically

Updates parameters using AdamW

Example output:

step 0: train loss 4.23, val loss 4.21
step 1000: train loss 2.45, val loss 2.50

✍️ Text Generation

After training, the model generates text autoregressively:

ROMEO:
What shall I do? O gentle night...


Generation uses probabilistic sampling from the model’s output distribution.

🧪 Key Learning Outcomes

Deep understanding of Transformer internals

How causal masking enables autoregressive generation

Why attention scaling stabilizes training

How context length impacts memory & compute

Difference between toy GPTs and large-scale production models

🚧 Limitations

Character-level tokenization (no BPE / SentencePiece)

No KV-cache or FlashAttention

Single-GPU / CPU training

Not intended for large-scale pretraining

This is a learning-focused NanoGPT, not a production LLM.

🔮 Future Improvements

Add subword tokenization (BPE)

Implement KV-cache for faster generation

Mixed-precision training (FP16)

Larger context window

Train on larger datasets
