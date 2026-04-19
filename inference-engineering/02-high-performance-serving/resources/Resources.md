# Phase 2: High-Performance Serving - Resources

This directory contains key resources for mastering high-throughput inference serving.

## Downloaded Resources

- **[Efficiently Serving LLMs through PagedAttention](./paged_attention.pdf)** (vLLM Paper)
  - *Description:* The seminal paper introducing PagedAttention, which solves the KV cache memory fragmentation problem and enables high-throughput serving.
- **[EAGLE: Speculative Decoding with Lookahead Batching](./eagle_speculative_decoding.pdf)**
  - *Description:* A advanced technique for speculative decoding that significantly increases throughput by predicting multiple tokens ahead.
- **[SGLang: Efficiently Serving LLMs with RadixAttention](./sglang_radix_attention.pdf)**
  - *Description:* Documentation of the RadixAttention technique for managing prefix caching across multiple requests.


## External Resources & Documentation

- **[vLLM Documentation](https://docs.vllm.ai/en/latest/)**
  - *Note:* The official architecture and deployment guide for the most popular open-source serving engine.
- **[NVIDIA Speculative Decoding (EAGLE-3)](https://developer.nvidia.com/blog/introduction-to-speculative-decoding/)**
  - *Note:* Technical breakdown of how to use a smaller "draft" model to speed up a larger "oracle" model.
- **[SGLang & RadixAttention](https://github.com/sgl-project/sglang)**
  - *Note:* A next-generation scheduling framework that uses a Trie-based KV cache management system (RadixAttention).
- **[Shared Memory IPC & gRPC](https://grpc.io/docs/what-is-grpc/introduction/)**
  - *Note:* Concepts for reducing the "latency tax" of data transfer between service layers.
