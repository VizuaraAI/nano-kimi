NanoKimiK2 vs NanoGPT: A Comparative Study
This repository contains a complete implementation of the NanoKimiK2 transformer model from scratch, designed to compete with the NanoGPT model. Both models are trained and evaluated on the TinyStories dataset to compare their performance in terms of loss, perplexity, and story generation capabilities.
Overview

NanoKimiK2: A custom-built transformer model incorporating Mixture of Experts (MoE), SwiGLU activation, RoPE (Rotary Position Embeddings), and MLAAttention mechanisms. It utilizes a novel Muon optimizer for enhanced training efficiency.
NanoGPT: A baseline transformer model inspired by the original GPT architecture, implemented for comparison purposes.
Dataset: TinyStories dataset, processed using SentencePiece tokenization.
Objective: Compare the training dynamics, validation metrics, and generative outputs of NanoKimiK2 against NanoGPT.

Features

Custom Components: Includes SwiGLU, MoELayer, MLAAttention, and a bespoke Muon optimizer.
Performance Optimization: Supports mixed precision training (bf16, fp16, fp32) with OOM retry mechanisms.
Evaluation Metrics: Tracks Negative Log Likelihood (NLL), Bits Per Character (BPC), perplexity, and auxiliary loss statistics.
Generation: Generates sample stories at regular intervals to assess qualitative performance.

Prerequisites

Python 3.8+
PyTorch
datasets (Hugging Face)
sentencepiece
numpy
matplotlib (for potential visualization)

Install dependencies via:
pip install torch datasets sentencepiece numpy matplotlib

Usage

Clone the Repository:
git clone https://github.com/yourusername/NanoKimiK2_vs_NanoGPT.git
cd NanoKimiK2_vs_NanoGPT


Run the Script:Execute the main script to train and compare both models:
python main.py


Configuration:

Adjust hyperparameters in the Runtime / Performance Configurations section of the code (e.g., BATCH_SIZE, EPOCHS, SEQ_LEN).
Enable/disable checkpointing with USE_CHECKPOINTING.


Output:

Training and validation losses are printed at intervals.
Sample story generations are displayed every STORY_GEN_INTERVAL steps.
Loss tables and VRAM usage are logged for analysis.



File Structure

main.py: Contains the complete implementation, including model definitions, training loop, and evaluation functions.

Results

Training Loss: Monitored for both models to compare convergence rates.
Validation Metrics: Perplexity, NLL, and BPC are evaluated to assess model performance.
Story Generation: Qualitative comparison of generated stories from both models.

Contributing
Contributions are welcome! Please fork the repository and submit pull requests for enhancements or bug fixes. Ensure to update the README with details of changes.
License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgments

Inspired by the original NanoGPT implementation by Andrej Karpathy.
Utilizes the TinyStories dataset from Hugging Face.
Thanks to the PyTorch community for robust tools and documentation.
