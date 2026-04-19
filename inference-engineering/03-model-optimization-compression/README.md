# Phase 3: Model Optimization (The "Compression" Manual)

**Goal:** Fitting "Size 10" models into "Size 2" hardware without losing intelligence.

## The Detailed Steps

- **Quantization Lab:** Implement Post-Training Quantization (PTQ). Learn the difference between Weight-Only (e.g., GPTQ) and Weight-Activation (e.g., SmoothQuant) quantization.

- **FP8 & NVFP4:** Study the new 4-bit and 8-bit floating point formats native to NVIDIA Blackwell (B200). Learn how to handle "Outliers"—the few neurons that have huge values and break standard quantization.

- **Sparsity Patterns:** Learn 2:4 Structured Sparsity. This is a hardware-level trick where the GPU skips every other calculation if the weight is zero.

- **Knowledge Distillation:** Build a pipeline where a "Teacher" model (GPT-4o) supervises the training of a "Student" (Llama-3-8B).

## Resources & Books

For convenience, key papers and documentation have been downloaded to the **[resources/](./resources/)** directory. See **[Resources.md](./resources/Resources.md)** for a full index.

- **[NEW] [Local Resource Index](./resources/Resources.md)**
- **Technical Whitepaper:** [NVIDIA Blackwell Architecture Whitepaper](./resources/nvidia_blackwell_architecture_whitepaper.pdf)
- **Handbook:** [BentoML: LLM Inference Handbook](https://bentoml.com/blog/llm-inference-handbook)
- **Paper:** [SmoothQuant: Post-Training Quantization for LLMs](./resources/smooth_quant.pdf)
- **Paper:** [GPTQ: Post-Training Quantization for Generative Pre-trained Transformers](./resources/gptq.pdf)
- **Paper:** [NVIDIA Blackwell Whitepaper](./resources/nvidia_blackwell_architecture_whitepaper.pdf)
- **Toolkit:** [NVIDIA TensorRT-Model Optimizer (ModelOpt)](https://nvidia.github.io/TensorRT-ModelOptimizer/)
