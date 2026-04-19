# Phase 4: Transformer Optimizations (The "Math" Manual)

## Goal
Rewriting the fundamental math of Attention to make it **O(n)** instead of **O(n^2)**.

## The Detailed Steps
- **FlashAttention-3 Implementation:** Understand the "Online Softmax" trick and how to use Tiling to keep all data in the GPU's SRAM.
- **Context Caching:** Implement RadixTree based caching for system prompts. If multiple users share a 5,000-token prompt, your server should only "think" about it once.
- **RoPE & Long Context:** Learn the math behind Rotary Positional Embeddings. Experiment with "YaRN" or "PI" to extend a model's context from 8k to 128k tokens without retraining.
- **Multi-Query Attention (MQA):** Learn why sharing "Keys" and "Values" across multiple "Heads" reduces memory bandwidth requirements.

## Resources & Books

For convenience, key papers and documentation have been downloaded to the **[resources/](./resources/)** directory. See **[Resources.md](./resources/Resources.md)** for a full index.

- **[NEW] [Local Resource Index](./resources/Resources.md)**
- **Paper:** [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](./resources/flash_attention.pdf)
- **Paper:** [YaRN: Efficient Context Window Extension of Large Language Models](./resources/yarn_context_window_extension.pdf)
- **Open Source:** [Dao-AILab/flash-attention GitHub](https://github.com/Dao-AILab/flash-attention)
- **Blog:** [Hugging Face: Optimizing Transformers for Long Context](https://huggingface.co/blog/optimizing-transformers-for-long-context)
