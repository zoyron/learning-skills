# Phase 2: High-Performance Serving (The "Throughput" Manual)

**Goal:** Building the "Engine" that manages thousands of concurrent requests without the system collapsing.

## The Detailed Steps

- **KV Cache Management:** Deep dive into *PagedAttention*. Understand how *vLLM* allocates non-contiguous memory blocks to store "Key-Value" pairs to prevent fragmentation.

- **Continuous Batching:** Implement a scheduler that can "preempt" a low-priority request for a high-priority one, or batch multiple users into a single GPU forward pass.

- **Speculative Decoding (EAGLE-3):** Learn to implement Draft-Verify loops. Use a lightweight 1B model to guess the next 5 tokens and use the 70B model to verify them in one parallel shot.

- **Request Orchestration:** Learn to use *gRPC* or *Shared Memory IPC* instead of standard REST/JSON. JSON parsing is a "latency tax" you can't afford.

## Resources & Books

For convenience, key papers and documentation have been downloaded to the **[resources/](./resources/)** directory. See **[Resources.md](./resources/Resources.md)** for a full index.

- **[NEW] [Local Resource Index](./resources/Resources.md)**
- **Technical Blog:** [NVIDIA Technical Blog: An Introduction to Speculative Decoding (EAGLE-3)](https://developer.nvidia.com/blog/introduction-to-speculative-decoding/)
- **Documentation:** [vLLM Architecture Deep Dive](https://docs.vllm.ai/en/latest/)
- **Paper:** [Efficiently Serving LLMs through PagedAttention](./resources/paged_attention.pdf)
- **Paper:** [EAGLE: Speculative Decoding with Lookahead Batching](./resources/eagle_speculative_decoding.pdf)
- **Paper:** [SGLang: Efficiently Serving LLMs with RadixAttention](./resources/sglang_radix_attention.pdf)

