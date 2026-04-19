# Phase 4: Transformer Optimizations - Resources

This directory contains resources focused on the mathematics and low-level kernel optimizations of the Transformer architecture.

## Downloaded Resources

- **[FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](./flash_attention.pdf)**
  - *Description:* The revolutionary paper that optimized attention by utilizing GPU SRAM tiling to minimize memory reads/writes.
- **[YaRN: Efficient Context Window Extension of Large Language Models](./yarn_context_window_extension.pdf)**
  - *Description:* Research paper detailng a method to extend the context window of existing models without retraining.


## External Resources & Documentation

- **[Dao-AILab/flash-attention GitHub](https://github.com/Dao-AILab/flash-attention)**
  - *Note:* The gold standard for high-performance attention kernels. Studying this code is essential for anyone writing custom CUDA/Triton kernels.
- **[Hugging Face: Optimizing Transformers for Long Context](https://huggingface.co/blog/optimizing-transformers-for-long-context)**
  - *Note:* A comprehensive blog post on YaRN, Positional Interpolation, and other RoPE scaling techniques.
- **[Context Caching & Radix Trees](https://github.com/vllm-project/vllm/blob/main/vllm/core/block_manager.py)**
  - *Note:* Reference implementation of how to "remember" long system prompts using prefix caching.
- **[YaRN: Efficient Context Window Extension](https://arxiv.org/abs/2309.00071)**
  - *Note:* Research paper on scaling context windows up to 128k+ tokens.
