# Phase 2: High-Performance Serving (The "Throughput" Manual)

**Goal:** Building the "Engine" that manages thousands of concurrent requests without the system collapsing.

## The Detailed Steps

- **KV Cache Management:** Deep dive into *PagedAttention*. Understand how *vLLM* allocates non-contiguous memory blocks to store "Key-Value" pairs to prevent fragmentation.

- **Continuous Batching:** Implement a scheduler that can "preempt" a low-priority request for a high-priority one, or batch multiple users into a single GPU forward pass.

- **Speculative Decoding (EAGLE-3):** Learn to implement Draft-Verify loops. Use a lightweight 1B model to guess the next 5 tokens and use the 70B model to verify them in one parallel shot.

- **Request Orchestration:** Learn to use *gRPC* or *Shared Memory IPC* instead of standard REST/JSON. JSON parsing is a "latency tax" you can't afford.

## Resources & Books

| Type | Title | Description |
|---|---|---|
| Documentation | [vLLM Architecture Deep Dive](https://example.com) | Official vLLM docs |
| Technical Blog | [NVIDIA Technical Blog: An Introduction to Speculative Decoding (EAGLE-3)](https://example.com) | In-depth article |
| Open Source | Study the source code of SGLang and its RadixAttention implementation |
| Research Paper | [Efficiently Serving LLMs through PagedAttention](https://example.com) | The original vLLM paper |
