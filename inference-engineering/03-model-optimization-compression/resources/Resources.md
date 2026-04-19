# Phase 3: Model Optimization - Resources

This directory contains key resources for model quantization, pruning, and structural optimization.

## Downloaded Resources

- **[SmoothQuant: Accurate and Efficient Post-Training Quantization for LLMs](./smooth_quant.pdf)**
  - *Description:* A popular technique for quantizing both weights and activations to 8-bit without losing accuracy.
- **[GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](./gptq.pdf)**
  - *Description:* A highly efficient weight-only quantization method that enables running massive models on single GPUs.
- **[NVIDIA Blackwell Architecture Whitepaper](./nvidia_blackwell_architecture_whitepaper.pdf)**
  - *Description:* Official NVIDIA document detailing the Blackwell architecture, including the new FP8 and NVFP4 numerical formats for AI inference.

## External Resources & Documentation


- **[LLM Inference Handbook by BentoML](https://bentoml.com/blog/llm-inference-handbook)**
  - *Note:* A great overview of the current landscape of model compression and serving.
- **[NVIDIA TensorRT-Model Optimizer (ModelOpt)](https://nvidia.github.io/TensorRT-ModelOptimizer/)**
  - *Note:* Official toolkit for PTQ (Post-Training Quantization) and QAT (Quantization-Aware Training) for NVIDIA hardware.
- **[AutoGPTQ GitHub](https://github.com/AutoGPTQ/AutoGPTQ)** / **[AutoAWQ GitHub](https://github.com/casper-hansen/AutoAWQ)**
  - *Note:* The two primary libraries for applying quantization to open-weights models.
- **[DeepLearning.ai: Compressed and Efficient AI Systems](https://www.deeplearning.ai/short-courses/compressed-and-efficient-ai-systems/)**
  - *Note:* Recommended course for theoretical foundations of model compression.
