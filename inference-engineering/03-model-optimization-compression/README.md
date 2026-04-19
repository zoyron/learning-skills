# Phase 3: Model Optimization (The "Compression" Manual)

**Goal:** Fitting "Size 10" models into "Size 2" hardware without losing intelligence.

## The Detailed Steps

- **Quantization Lab:** Implement Post-Training Quantization (PTQ). Learn the difference between Weight-Only (e.g., GPTQ) and Weight-Activation (e.g., SmoothQuant) quantization.

- **FP8 & NVFP4:** Study the new 4-bit and 8-bit floating point formats native to NVIDIA Blackwell (B200). Learn how to handle "Outliers"—the few neurons that have huge values and break standard quantization.

- **Sparsity Patterns:** Learn 2:4 Structured Sparsity. This is a hardware-level trick where the GPU skips every other calculation if the weight is zero.

- **Knowledge Distillation:** Build a pipeline where a "Teacher" model (GPT-4o) supervises the training of a "Student" (Llama-3-8B).

## Resources & Books

| Type | Title | Description |
|---|---|---|
| Handbook | LLM Inference Handbook by BentoML | Comprehensive guide on quantization |
| GitHub | AutoGPTQ and AutoAWQ repositories | Repositories for quantization tools |
| Documentation | NVIDIA TensorRT-Model Optimizer (ModelOpt) API | Official API documentation |
| Course | DeepLearning.ai: Compressed and Efficient AI Systems | Educational course |
