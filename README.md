🌟 NanoKimiK2 vs NanoGPT: A Thrilling Transformer Showdown! 🌟
Welcome to the electrifying world of AI language models! This repository showcases a ground-up implementation of the innovative NanoKimiK2 transformer, pitted against the classic NanoGPT in a head-to-head battle. Trained on the whimsical TinyStories dataset, these models compete to deliver the best in loss metrics, perplexity, and creative storytelling. Get ready for an exciting journey into the future of natural language processing!
🚀 Project Highlights

NanoKimiK2: A custom-built marvel featuring Mixture of Experts (MoE), SwiGLU activation, RoPE (Rotary Position Embeddings), and MLAAttention. Powered by a cutting-edge Muon optimizer for top-notch training efficiency.
NanoGPT: The legendary baseline transformer, reimagined for this epic comparison.
Dataset: The charming TinyStories dataset, tokenized with SentencePiece for a fair fight.
Goal: Unleash a showdown of training dynamics, validation prowess, and generative flair!

🎨 Key Features

Innovative Design: Packed with SwiGLU, MoELayer, MLAAttention, and a bespoke Muon optimizer.
Performance Boost: Supports mixed precision training (bf16, fp16, fp32) with smart OOM retry logic.
Insightful Metrics: Tracks Negative Log Likelihood (NLL), Bits Per Character (BPC), perplexity, and auxiliary loss stats.
Creative Sparks: Generates dazzling sample stories at regular intervals to showcase qualitative magic.

🛠️ Getting Started
Prerequisites

Python 3.8+
PyTorch
datasets (Hugging Face)
sentencepiece
numpy
matplotlib (for stunning visualizations)

Fire up your setup with:
pip install torch datasets sentencepiece numpy matplotlib

How to Run

Clone the Repo:
git clone https://github.com/yourusername/NanoKimiK2_vs_NanoGPT.git
cd NanoKimiK2_vs_NanoGPT


Launch the Magic:
python main.py


Tweak the Fun:

Adjust hyperparameters in the Runtime / Performance Configurations section (e.g., BATCH_SIZE, EPOCHS, SEQ_LEN).
Toggle checkpointing with USE_CHECKPOINTING.


Watch the Show:

Enjoy live updates of training and validation losses.
Marvel at story generations every STORY_GEN_INTERVAL steps.
Dive into loss tables and VRAM usage for a deep dive.



📂 File Structure

main.py: The heart of the action, housing model definitions, training loops, and evaluation wizardry.

📊 Results to Expect

Training Loss: Witness the convergence race between NanoKimiK2 and NanoGPT.
Validation Metrics: Feast your eyes on perplexity, NLL, and BPC to judge the champs.
Story Generation: Revel in the creative tales spun by both models.

🤝 Contribute to the Epic
Love the vibe? Fork this repo and send pull requests with your enhancements or bug fixes. Update this README with your heroic contributions!
📜 License
This project rocks under the MIT License - check out the LICENSE file for the fine print.
🙌 Shoutouts

Inspired by the genius of NanoGPT by Andrej Karpathy.
Powered by the TinyStories dataset from Hugging Face.
Big thanks to the PyTorch community for their awesome tools and docs!
