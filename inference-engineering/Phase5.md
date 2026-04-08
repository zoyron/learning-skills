# Phase 5: Edge AI (The "Frontier" Manual)

## Goal
Running the world's most powerful models on a phone or a laptop with zero cloud dependency.

## The Detailed Steps
- **Apple MLX Mastery:** Learn the Unified Memory Architecture. Write a script in MLX to run a model where the CPU and GPU share the same memory pointer (Zero-Copy).
- **WebGPU Inference:** Learn to write WGSL (WebGPU Shading Language). Port a small Transformer model to run in a browser using ONNX Runtime Web.
- **ExecuTorch Deployment:** Learn to "Lower" a PyTorch graph into a flatbuffer file that can be executed on an iPhone's NPU (Neural Processing Unit).
- **Thermal Throttling Management:** Learn to monitor chip temperature and dynamically switch to a smaller "Draft" model if the device gets too hot.

## Resources & Books
| Resource Type | Description |
| --- | --- |
| Framework | Apple Machine Learning Research: MLX Documentation |
| Tutorial | WebGPU for AI Inference (Available on core.cz or Google Developer blogs) |
| Documentation | ExecuTorch 1.0 GA Documentation (Meta) |
| Project | Study the llama.cpp source code. It is the gold standard for portable, CPU-based inference |

## Final HFT Insight
> In HFT, the best code is the code that never runs. In Inference, the best optimization is the token that never has to be computed. Use caching and speculative decoding to cheat the system.
