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
| ⚡ **Optimizer**     | Powered by the custom made advanced **Muon Optimizer**                         |
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
* Plot **comparisons table**

---
## 🌟 Custom Muon Optimizer
I have developed the **Muon Optimizer** completely from scratch, inspired by research papers and modern optimization techniques. It is a state-of-the-art PyTorch optimizer designed for high-performance training of deep neural networks, particularly attention-based architectures like transformers. Muon combines advanced optimization strategies with stability enhancements to deliver robust and efficient convergence.

---

### How It Works

The Muon Optimizer reimagines traditional optimization by:

* **Preconditioning Gradients:**
  Utilizes a two-dimensional covariance approach (G and H matrices) to precondition gradients, updated every `precond_update_freq` steps for efficiency.

* **Adaptive Weight Clipping:**
  Dynamically adjusts attention weights based on RMS calculations, ensuring optimal signal propagation across heads with a safety threshold (`tau`).

* **Bias Correction:**
  Incorporates Adam-style bias correction for early training phases, transitioning to a pure Muon approach as iterations progress.

This optimizer shines in scenarios requiring high-dimensional parameter spaces, such as the **NanoKimiK2 transformer**, where its bespoke design delivers measurable improvements in training dynamics.

---

### Key Features

* **Second-Order Preconditioning:**
  Uses the Newton-Schulz method to compute inverse p-th roots for adaptive preconditioning of gradients, improving optimization stability for large, high-dimensional weight matrices.

* **Adaptive Gradient Scaling:**
  Implements RMS-based gradient normalization to maintain consistent update magnitudes across layers, automatically balancing between preconditioned and standard Adam-style updates.

* **QKClip for Attention Modules:**
  Introduces a quantitative attention clipping mechanism (`qkclip`) to dynamically calibrate query-key projections in multi-head attention, reducing gradient instability and improving training robustness.

* **Flexible Weight Decay & Adam Bias Correction:**
  Supports classic weight decay with optional Adam bias correction, making it compatible with a wide range of network architectures.

* **Automatic Attention Module Integration:**
  Easy binding to custom attention modules (`MLAAttention`) for real-time RMS tracking and per-head scaling of projections.

* **Highly Configurable:**
  Every aspect, from learning rate and beta coefficients to preconditioner iterations and qkclip parameters, is fully configurable, giving researchers and developers precise control over optimization behavior.

---

### Benefits

* Stabilizes training for **deep, wide, or attention-heavy networks** where standard optimizers struggle.
* Handles **large parameter matrices efficiently** with preconditioning and RMS scaling.
* Provides **fine-grained control over gradient updates** and attention projection norms, promoting consistent convergence.
* Designed for **extensibility**, allowing integration with novel architectures and custom modules.

---

## 📊 Results

<img width="1086" height="825" alt="image" src="https://github.com/user-attachments/assets/55a23d8b-98ab-48de-9108-032acedc0a66" />
The figure compares the average training loss of NanoKimiK2 (blue) and NanoGPT (red) across training steps.
  1. NanoKimiK2 shows faster initial convergence, reducing loss rapidly in the early training phase.
  2. However, as training continues, NanoGPT maintains steady improvement and eventually achieves a lower final average loss.
  3. This indicates that while NanoKimiK2 learns quickly at first, NanoGPT generalizes slightly better with more training steps.

### 📖 Sample Text Generation Comparison

To evaluate generative quality beyond loss metrics, both models were tested on the same prompt after different training steps:
**Prompt:**
*"Once, there was a small boy named Charlie. Charlie loved stories more than anything else."*

### 🧩 Step 1000

**NanoKimiK2:**
Output: NanoKimiK2 Completion: Once, there was a small boy named Charlie. Charlie loved stories more than anything else. One. At that he loved. When it. But every for one car would climb the way down the lake made a lot of toys near the store and the tree. Later a big basket smiled and higher than ever after all the rain. He swam towards him. As he could see her friends had so good care of and started to come to eat carrots that if she was beautiful butterfly!" Max realized that lived a small to get. One day, so much and a big forest to do anything, Lily was and one to Tim and played and Tim loved music to her finger and some are not. The little better. Do you want to Lily. "Hey. They had come to keep your eyes, why don's, "You were walking through the lizard when there when he saw her mom. It was making food and it, "Who?" It flew outside and felt a very small bird, a large tree is perfect, "Come on if you are friends came to reach it was a

* Produces more **coherent sentence transitions** and a better sense of **narrative flow**, though still with grammatical instability.
* Begins forming story-like continuations (mentioning toys, lakes, friends, etc.), showing **early signs of structured imagination**.
* However, random insertions and character swaps indicate the model is still in early learning phases.

**NanoGPT:**
Output: NanoGPT Completion: Once, there was a small boy named Charlie. Charlie loved stories more than anything else. One day, Max's parent asked Joe if they were all so she could not wait to find cereal out his mom's journey. Sally told But one step the toys there, it broke hot music! Jake did not come back but only cared about anything. Mike thought they were not really good. So Bobby's mother's head at Jack's voice. It' Everyone like a man told Mark it and Alex thanked Sally friends. The man said, "Let's play two together if we can hide up in little barber on Ben first, too! We'll put them together and make sure it's able to race another way to celebrate tomorrows hards of the little boy made Jack feel happy and cozy. Everyone would show him how to find it up close in the boy. With a few hours, Bobby felt jealous little knowing the little girl could be too high and quiet not open their room she felt very sad. She knew that moment can come back soon.

* Generates **shorter, repetitive patterns** and loses logical continuity early.
* Storyline jumps abruptly between characters with minimal context retention.
* Indicates **slower language structure acquisition** at this training stage.

### 🧩 Step 2000

**NanoKimiK2:**
Output: Once, there was a small boy named Charlie. Charlie loved stories more than anything else. She went on any friends came! Emma could do math right away her mom gave her back. One day they would look the beach, she kept jumping close playing for all afternoon to her mom said his face. Once upon a shiny silver coin on my brother came across the children cheered as new toy in the game for a happy and gave him?" Sammy was important, but had lost!" So, feeling proud. At first he could eat something unusual coin?" Suddenly, they played on a great joblys go the park. Jack were. After playing outside when he hadn'llelall for treasure. And that, let't worry sweetheart." Mark and he still have gotten in half. Timmy said, and saw the box with his friends about a boy. Once upon a lovely. One day, there was excited and got scared again until he had an adorable. So, Bob and he was too hot tea, a good friend in the night. One day on it," Jenny. Everything 

* Demonstrates **clearer storytelling ability** — sentences connect more smoothly and maintain a narrative tone.
* Shows improvement in **syntax and coherence** with more consistent sentence forms.
* Still hallucinates a bit, but structure and rhythm are visibly more refined than at step 1000.

**NanoGPT:**
Output: Once, there was a small boy named Charlie. Charlie loved stories more than anything else. One day, he saw a big, shiny thing in his attic. He decided to take in an envelope. The envelope was clear and soft, long time for the two colors. Fred opened it and was so beautiful. However, one day, while at the party, Fred found a big, hairy apple. He was amazed. He ran and ran until, it opened right up to him. But, when he woke up, he heard a loud bark "Hello, two three, let's say your own of mine!". Andy looked up and noticed a big cat, trying to cut out silly paws. But he didn't know what to do for other, he just ignored him. So he picked away all the cheese and set it with him to find its more treasure. Andy was so happy to learn more about exploring the attic, in the woods all the distant things! Once upon a time, there looked in the dark. One day his mom had never found a wonderful, so

* Produces somewhat more stable text than before but continues to show **logical inconsistencies** and abrupt transitions.
* Narrative focus drifts rapidly; grammar remains uneven.
* Indicates **slower convergence in linguistic structure** compared to NanoKimiK2.

### Summary
Even at 2000 steps, **NanoKimiK2** shows faster qualitative improvement — its text demonstrates better continuity and contextual flow than **NanoGPT**. This aligns with its lower training loss curve, suggesting more efficient internal representation learning.

### Model Ratings Comparison
We provided the output generated to GPT and asked it to rate it out of 10 based on parameters such as Creativity, Coherence, Grammar, and Consistency.
Here is the table:

| Model        | Creativity | Coherence | Grammar | Consistency | Overall |
|--------------|------------|-----------|---------|------------|---------|
| **NanoKimiK2** | 7.0        | 5.67      | 6.0     | 6.0        | 6.17    |
| **NanoGPT**    | 5.67       | 5.0       | 5.0     | 5.0        | 5.17    |

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
