# 🌟 NanoKimiK2 vs NanoGPT: A Thrilling Transformer Showdown

Welcome to the world of **AI language models** — where innovation meets storytelling!
This repository presents a **from-scratch implementation** of the cutting-edge **NanoKimiK2 Transformer**, competing head-to-head with the classic **NanoGPT**.
Both models are trained on the whimsical **TinyStories dataset**, battling for supremacy in **loss metrics, perplexity, and creative generation**.

---

## 🚀 Project Overview

### 🧠 Models

* **NanoKimiK2** – A modern transformer powered by:

  * Mixture of Experts (**MoE**)
  * **SwiGLU** activation
  * **Rotary Position Embeddings (RoPE)**
  * **MLA Attention**
  * Optimized with the **Muon optimizer** for superior training performance.
* **NanoGPT** – The legendary minimal GPT baseline, reborn for a fair comparison.

### 🎯 Goal

To explore, visualize, and compare the **training dynamics**, **validation performance**, and **creative generation** abilities of both transformers.

---

## 🎨 Key Features

* **Innovative Architecture:**
  Integrates SwiGLU, MoELayer, MLA Attention, and Muon optimization for high performance.

* **Mixed Precision Training:**
  Supports `bf16`, `fp16`, and `fp32` modes with intelligent **Out-of-Memory (OOM) retry logic**.

* **Comprehensive Metrics:**
  Tracks **Negative Log Likelihood (NLL)**, **Bits Per Character (BPC)**, **perplexity**, and **auxiliary losses**.

* **Generative Showcase:**
  Produces **sample stories** at regular intervals — giving qualitative insight into each model’s creativity.

---

## 🛠️ Getting Started

### Prerequisites

Ensure you have the following installed:

```bash
Python 3.8+
PyTorch
datasets
sentencepiece
numpy
matplotlib
```

### Installation

Install dependencies using:

```bash
pip install torch datasets sentencepiece numpy matplotlib
```

---

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/NanoKimiK2_vs_NanoGPT.git
cd NanoKimiK2_vs_NanoGPT
```

### 2. Launch Training

```bash
python main.py
```

### 3. Adjust Configurations

Modify hyperparameters inside the configuration section (e.g. `BATCH_SIZE`, `EPOCHS`, `SEQ_LEN`).
Enable or disable checkpointing via `USE_CHECKPOINTING`.

### 4. Monitor Progress

* Live tracking of **training and validation losses**
* Periodic **story generations**
* Detailed **loss tables** and **VRAM utilization insights**

---

## 📂 Project Structure

```
NanoKimiK2_vs_NanoGPT/
│
├── main.py                # Core logic: model definition, training, evaluation
├── configs/               # Configuration files (if any)
├── checkpoints/           # Model checkpoints
├── data/                  # Tokenized TinyStories dataset
└── README.md              # Documentation
```

---

## 📊 Expected Results

| Metric                | NanoKimiK2            | NanoGPT                |
| --------------------- | --------------------- | ---------------------- |
| Training Loss         | ⚡ Rapid convergence   | Steady baseline        |
| Validation Perplexity | 🔥 Lower values       | Moderate               |
| Creativity            | ✨ More dynamic & rich | Consistent but simpler |

Enjoy visualizations of loss curves and generated text samples as the models evolve!

---

## 🤝 Contributing

Contributions are welcome!
If you’d like to improve the implementation or add new experiments:

1. Fork the repository
2. Create a new branch
3. Submit a pull request

Please also update this README to reflect your contributions.

---

## 📜 License

This project is licensed under the **MIT License**.
Refer to the [LICENSE](./LICENSE) file for details.

---

## 🙌 Acknowledgements

* Inspired by **[NanoGPT](https://github.com/karpathy/nanoGPT)** by *Andrej Karpathy*
* Dataset: **TinyStories** from *Hugging Face*
* Gratitude to the **PyTorch community** for their incredible tools and documentation


