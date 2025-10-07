# 🌟 **NanoKimiK2 vs NanoGPT: A Transformer Showdown**

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/PyTorch-2.2+-ee4c2c?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/Python-3.8+-yellow.svg" alt="Python">
  <img src="https://img.shields.io/badge/Dataset-TinyStories-9cf" alt="Dataset">
  <img src="https://img.shields.io/badge/HuggingFace-Compatible-orange.svg" alt="Hugging Face">
</p>

A **complete open-source framework** to train, compare, and analyze **NanoKimiK2** and **NanoGPT** — two small yet powerful transformer architectures designed for creativity and research.

---

## 🎯 The Mission: Open-Source Transformer Innovation

When open-weight models like *NanoGPT* arrived, they inspired a wave of innovation — but few projects offered **fully open, reproducible training frameworks**.

**NanoKimiK2_vs_NanoGPT** bridges that gap.
It provides an **end-to-end codebase** for training, evaluation, and benchmarking of two models:

* **NanoGPT** – the classic baseline
* **NanoKimiK2** – a next-gen experimental architecture with modern design features like **Mixture of Experts**, **SwiGLU**, and **RoPE**

This isn’t just a model comparison — it’s an exploration into **what makes transformers learn, reason, and create**.

---

## ⚙️ Core Features

| Category            | Description                                                                 |
| ------------------- | --------------------------------------------------------------------------- |
| 🚀 **Performance**  | Mixed precision training (`bf16`, `fp16`, `fp32`) with auto OOM retry logic |
| 🧠 **Architecture** | NanoKimiK2 integrates **MoE**, **SwiGLU**, **MLAAttention**, and **RoPE**   |
| ⚡ **Optimizer**     | Powered by the efficient **Muon Optimizer**                                 |
| 📊 **Metrics**      | Tracks **NLL**, **BPC**, **Perplexity**, and auxiliary losses               |
| ✨ **Creativity**    | Periodic **story generation** for qualitative insight                       |
| 🧩 **Configurable** | Fully modular — tweak batch size, sequence length, epochs, and checkpoints  |

---

## 🧰 Project Structure

```
├── main.py                # Core training loop, evaluation, and model logic
├── configs/               # Model & training hyperparameter configs
├── data/                  # Tokenized TinyStories dataset
├── checkpoints/           # Model checkpoints
├── results/               # Logs, plots, and generated stories
├── LICENSE
└── README.md
```

---

## 🚀 Getting Started

### **Step 1: Setup Environment**

```bash
git clone https://github.com/yourusername/NanoKimiK2_vs_NanoGPT.git
cd NanoKimiK2_vs_NanoGPT
pip install torch datasets sentencepiece numpy matplotlib
```

---

### **Step 2: Train the Models**

Launch the training loop for both models:

```bash
python main.py
```

Customize key parameters inside the configuration block:

* `BATCH_SIZE`
* `SEQ_LEN`
* `EPOCHS`
* `USE_CHECKPOINTING`

---

### **Step 3: Monitor the Showdown**

During training:

* Observe **training/validation losses**
* View **real-time story generations**
* Analyze **loss tables**, **VRAM usage**, and **metric curves**

---

## 📊 Sample Results

| Metric                 | Description                                        |
| ---------------------- | -------------------------------------------------- |
| **Training Loss**      | Compare convergence between NanoKimiK2 and NanoGPT |
| **Validation Metrics** | Observe Perplexity, NLL, and BPC                   |
| **Generated Stories**  | Witness qualitative improvement across epochs      |

Sample stories are automatically saved under the `results/` directory — allowing you to track creative evolution step-by-step.

---

## 🧪 Example Commands

Train specific models:

```bash
python main.py --model nanogpt --epochs 15 --batch_size 8
python main.py --model nanokimik2 --epochs 15 --batch_size 8
```

Enable gradient checkpointing for large runs:

```bash
USE_CHECKPOINTING=True python main.py
```

---

## 🔭 Watching the Models Learn

Over training, both models evolve from simple word associations to coherent storytelling.
The **NanoKimiK2** model often exhibits sharper syntax consistency and thematic depth due to its SwiGLU + MoE combination.

Visual comparisons (training curves, story snapshots, perplexity evolution) can be found in the `results/` directory.

---

## 🧭 Roadmap

* [ ] Add **FSDP** and **DeepSpeed** support for large-scale training
* [ ] Implement **quantization-aware training**
* [ ] Integrate **TensorBoard/W&B** dashboards
* [ ] Extend to **multi-lingual TinyStories** dataset
* [ ] Publish **pre-trained checkpoints** on Hugging Face Hub

---

## 🤝 Contributing

We welcome community contributions!
To contribute:

1. **Fork** this repository
2. Create a feature branch → `feature/your-feature`
3. **Commit**, **push**, and open a Pull Request

Please maintain clean, modular code and include comments for readability.

---

## 📜 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for more details.

---

## 🙌 Acknowledgements

* Inspired by **NanoGPT** by *Andrej Karpathy*
* Dataset: **TinyStories** (Hugging Face)
* Framework: **PyTorch**
* Developed by **Devashish Gaikwad (2025)**

---

## 📚 Citation

If you find this project useful for your research or experiments, please cite:

```bibtex
@software{Devashish_NanoKimiK2_vs_NanoGPT_2025,
  author = {Devashish Gaikwad},
  title = {{NanoKimiK2 vs NanoGPT: A Comparative Study of Transformer Architectures}},
  month = {October},
  year = {2025},
  url = {https://github.com/yourusername/NanoKimiK2_vs_NanoGPT}
}
```

