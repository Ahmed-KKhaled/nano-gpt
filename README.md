# GPT From Scratch (nanoGPT Implementation)

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-EE4C2C?logo=pytorch&logoColor=white)
![Transformer](https://img.shields.io/badge/Architecture-Decoder--Only%20Transformer-success)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

# 📌 Overview

This project is an educational implementation of a **GPT-style Language Model** built entirely in **PyTorch** following **Andrej Karpathy's nanoGPT** series.

The objective of this project is to understand every component of the Transformer architecture by implementing it from scratch instead of relying on high-level libraries.

The model is trained as a **character-level autoregressive language model** on the **Tiny Shakespeare** dataset and generates text one character at a time.

---

# 🧠 Model Architecture

The model follows the **Decoder-Only Transformer** architecture.

### Architecture Pipeline

```

Input Tokens
↓
Token Embedding
+
Positional Embedding
↓
N × Transformer Blocks

* LayerNorm
* Masked Multi-Head Self Attention
* Residual Connection
* LayerNorm
* Feed Forward Network
* Residual Connection

↓
Final LayerNorm
↓
Linear Language Modeling Head
↓
Softmax
↓
Next Character Prediction

```

---

# ⚙️ Core Components

### 🔹 Token Embedding
Maps each character into a learnable embedding vector.

### 🔹 Positional Embedding
Injects positional information so the model understands token order.

### 🔹 Masked Self-Attention
Implements causal attention so each token can only attend to previous tokens.

### 🔹 Multi-Head Attention
Allows the model to learn multiple relationships simultaneously by attending from different representation subspaces.

### 🔹 Feed Forward Network
Processes each token independently after attention to improve feature representation.

### 🔹 Residual Connections
Improves gradient flow and stabilizes deep Transformer training.

### 🔹 Layer Normalization
Normalizes activations before each sub-layer (Pre-LayerNorm).

### 🔹 Dropout
Reduces overfitting during training.

### 🔹 Weight Initialization
Uses GPT-style weight initialization for stable optimization.

---

# 📂 Dataset

The model is trained on the famous **Tiny Shakespeare** dataset.

Dataset contains:

- Shakespeare plays
- Character-level text
- Around 1 Million characters

---

# 🏗️ Training Pipeline

1. Load Tiny Shakespeare dataset
2. Build character vocabulary
3. Create input-target token pairs
4. Initialize GPT model
5. Train using Cross Entropy Loss
6. Optimize using AdamW
7. Evaluate Train / Validation Loss
8. Generate new text autoregressively

---

# 📊 Training Configuration

| Hyperparameter | Value |
|---------------|------:|
| Batch Size | 64 |
| Block Size | 256 |
| Embedding Size | 384 |
| Number of Heads | 6 |
| Number of Layers | 6 |
| Dropout | 0.2 |
| Optimizer | AdamW |
| Learning Rate | 3e-4 |

---

# 🔍 Implemented Concepts

✅ Character Tokenization

✅ Token Embeddings

✅ Positional Embeddings

✅ Masked Self Attention

✅ Multi Head Attention

✅ Feed Forward Network

✅ Layer Normalization

✅ Residual Connections

✅ Transformer Blocks

✅ GPT Text Generation

✅ Weight Initialization

---

# ✨ Example Generated Text

```

ROMEO:
What shall I say unto the king?
My heart is full of sorrow...

```

*(Generated after training on Tiny Shakespeare)*

---

# ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/YourUsername/gpt-from-scratch.git

cd gpt-from-scratch
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

#  Usage

###  Train & Generate Text

```bash
python gpt.py
```

---

# 📁 Project Structure

```

nano-gpt/

│

├── input.txt # data 
├── gpt.py
├── requirements.txt
└── README.md

```

---

#  What I Learned

During this project I implemented and understood:

- Transformer Decoder architecture
- Self-Attention mechanism
- Multi-Head Attention
- Feed Forward Networks
- Residual Connections
- Layer Normalization
- Positional Embeddings
- GPT Autoregressive Generation
- Weight Initialization
- Language Modeling with Cross Entropy Loss

---

#  Future Improvements

- Flash Attention
- Rotary Positional Embeddings (RoPE)
- KV Cache
- Mixed Precision Training
- Gradient Accumulation
- Larger Datasets
- GPT-2 Weight Loading
- Fine-tuning Support

---

# 📖 References

- Attention Is All You Need (2017)
- nanoGPT — Andrej Karpathy
- The Illustrated Transformer
- PyTorch Documentation

---

# 🛠️ Tech Stack

- Python
- PyTorch
---

# 📬 Contact

If you have any questions or suggestions, feel free to reach out!

📧 ahmedkhaled5.ml@gmail.com

---

<p align="center">
Built for learning ❤️ | Inspired by Andrej Karpathy's nanoGPT
</p>
