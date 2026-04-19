# Phase 5: Edge AI & Browser Deployment - Resources

This directory contains resources for deploying and optimizing models on local devices (Phones, Laptops, Browsers).

## Downloaded Resources

- **[LLM.int8(): 8-bit Matrix Multiplication for Transformers at Scale](./llm_int8_quantization.pdf)**
  - *Description:* The foundational paper for modern 8-bit quantization techniques used in local inference tools like bitsandbytes and llama.cpp.

## External Frameworks & Documentation


- **[Apple MLX Framework](https://ml-explore.github.io/mlx/)**
  - *Note:* The primary library for running optimized inference on Apple Silicon (M1/M2/M3/M4) using Unified Memory.
- **[ExecuTorch Documentation (Meta)](https://pytorch.org/executorch/stable/index.html)**
  - *Note:* Meta's official framework for deploying PyTorch models to edge devices (iOS, Android, and embedded systems).
- **[WebGPU for AI Inference (web.dev)](https://web.dev/articles/gpu-compute)**
  - *Note:* Google's developer guide for using the browser's GPU for compute tasks, including LLM inference.
- **[llama.cpp GitHub](https://github.com/ggerganov/llama.cpp)**
  - *Note:* The gold standard for cross-platform, CPU-based local inference. Essential for understanding low-level quantization for edge devices (GGUF).
- **[ONNX Runtime Web](https://onnxruntime.ai/docs/tutorials/web/)**
  - *Note:* Guide for running models in the browser with hardware acceleration.

## Advanced Topics

- **Thermal Management & Dynamic Loading**
  - *Note:* Concept of monitoring device temperature and switching between full-size and "draft" models to prevent hardware throttling on mobile.
- **Zero-Copy Memory Access**
  - *Note:* Understanding how Unified Memory architectures (Apple Silicon) allow the CPU and GPU to share the same physical memory pointers for zero-latency data transfer.
