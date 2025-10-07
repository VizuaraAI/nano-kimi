Perfect 👌 Since everything is inside **one Jupyter notebook** and not in multiple folders or `.py` files, here’s your **final, polished, professional README** — clean, structured, and fully aligned with your GitHub repo setup (`https://github.com/VizuaraAI/nano-kimi`):

---

# 🌟 **NanoKimiK2 vs NanoGPT: A Transformer Showdown**

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/PyTorch-2.2+-ee4c2c?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/Python-3.8+-yellow.svg" alt="Python">
  <img src="https://img.shields.io/badge/Dataset-TinyStories-9cf" alt="Dataset">
  <img src="https://img.shields.io/badge/HuggingFace-Compatible-orange.svg" alt="Hugging Face">
</p>

A **complete open-source framework** to train, compare, and analyze **NanoKimiK2** and **NanoGPT**, two compact yet powerful transformer architectures designed for research and creative text generation.

---

## 🎯 The Mission: Open-Source Transformer Innovation

When open-weight models like *NanoGPT* appeared, they sparked a wave of innovation — but few offered **fully open, reproducible training frameworks**.

**NanoKimiK2 vs NanoGPT** bridges that gap.
This repository provides an **end-to-end, Jupyter-based implementation** for training, evaluation, and benchmarking of two models:

* **NanoGPT** – The classic minimal GPT baseline
* **NanoKimiK2** – A next-generation architecture featuring **Mixture of Experts**, **SwiGLU**, **RoPE**, and **MLA Attention**

This project is not just a comparison — it’s an exploration into **how transformer design choices influence learning, reasoning, and creativity**.

---

## ⚙️ Core Features

| Category            | Description                                                                     |
| ------------------- | ------------------------------------------------------------------------------- |
| 🚀 **Performance**  | Mixed precision training (`bf16`, `fp16`, `fp32`) with auto OOM retry logic     |
| 🧠 **Architecture** | NanoKimiK2 integrates **MoE**, **SwiGLU**, **MLAAttention**, and **RoPE**       |
| ⚡ **Optimizer**     | Powered by the advanced **Muon Optimizer**                                      |
| 📊 **Metrics**      | Tracks **NLL**, **BPC**, **Perplexity**, and auxiliary losses                   |
| ✨ **Creativity**    | Periodic **story generation** for qualitative analysis                          |
| 🧩 **Configurable** | Hyperparameters like batch size, epochs, and sequence length are easily tunable |

---

## 🚀 Getting Started

### **Step 1: Setup Environment**

```bash
git clone https://github.com/VizuaraAI/nano-kimi.git
cd nano-kimi
pip install torch datasets sentencepiece numpy matplotlib
```

---

### **Step 2: Open the Notebook**

Since this project is implemented in a **single Jupyter Notebook**, launch Jupyter and open the notebook file:

```bash
jupyter notebook
```

Then open the main notebook (e.g. `nano-kimi.ipynb`) and **run all cells sequentially**.

This will:

* Train **NanoKimiK2** and **NanoGPT**
* Display real-time **training and validation metrics**
* Generate **sample stories**
* Plot **loss curves and comparisons**

---

## 📊 Sample Results

| Metric                 | Description                                     |
| ---------------------- | ----------------------------------------------- |
| **Training Loss**      | Observe convergence speed between both models   |
| **Validation Metrics** | Compare Perplexity, NLL, and BPC values         |
| **Generated Stories**  | Evaluate qualitative improvements across epochs |

You can visualize loss trends and sample generations directly inside the notebook’s output cells.

---

## 🔭 Observations

Over training, both models evolve from simple word associations to coherent storytelling.
**NanoKimiK2**, due to its **SwiGLU + MoE** combination, often demonstrates:

* Smoother loss convergence
* Richer narrative structure
* Improved contextual recall

---

## 🧭 Roadmap

* [ ] Add **FSDP / DeepSpeed** support for scalable experiments
* [ ] Integrate **TensorBoard / W&B** logging
* [ ] Explore **quantization-aware training**
* [ ] Extend to **multi-lingual TinyStories**
* [ ] Publish **pre-trained weights** on Hugging Face Hub

---

## 🤝 Contributing

Contributions are welcome!
To contribute:

1. **Fork** this repository
2. Create a branch → `feature/your-feature-name`
3. Commit and **open a Pull Request**

Please maintain clean, modular code and meaningful comments.

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

If you use or refer to this project, please cite:

```bibtex
@software{Devashish_NanoKimiK2_vs_NanoGPT_2025,
  author = {Devashish Gaikwad},
  title = {{NanoKimiK2 vs NanoGPT: A Comparative Study of Transformer Architectures}},
  month = {October},
  year = {2025},
  url = {https://github.com/VizuaraAI/nano-kimi}
}
```

---

Would you like me to add a **“Notebook Preview” section** with a thumbnail (like a screenshot of a training cell or graph) that links directly to your `.ipynb` file? It looks great on GitHub and attracts readers instantly.
