# MIT 6.172: ML Infrastructure Transition Guide

## Objective
Utilize MIT 6.172 (Performance Engineering of Software Systems) to master the C++ performance skills required for the ML Serving Layer. Zero ML math required.

## Curriculum to ML Infra Mapping

* **Memory Hierarchy & Caching (Lectures 2-4, 13)**
  * *ML Application:* Optimizing memory-bound Large Language Model (LLM) inference (e.g., KV Cache). Essential for engines like vLLM and ONNX Runtime. Focus on spatial and temporal locality.
* **Vectorization & SIMD (Lectures 7-8)**
  * *ML Application:* Hardware-level matrix multiplication execution. Teaches multi-data operations in single clock cycles (AVX-512) before scaling to GPU architecture.
* **Multithreading & Synchronization (Lectures 10-12, 14-15)**
  * *ML Application:* Managing high-throughput, concurrent API requests for serving systems. Focus on lock-free programming and thread pool management.
* **Profiling & Tooling (Throughout)**
  * *ML Application:* Identifying inference pipeline stalls. Requires mastery of `perf`, `Cachegrind`, and `Valgrind`.

## Execution Strategy (via MIT OCW)

Assignments are mandatory for practical application. 

1. **Project 1: Bit Hacks & Matrix Multiplication**
   * Foundational skill for understanding how machine learning models execute at the hardware level.
2. **Project 2: Memory Allocator (Custom `malloc`)**
   * Critical for deep understanding of memory management, required for handling limited GPU VRAM and optimizing host-to-device memory transfers.
3. **Final Project: Leiserchess**
   * Maps directly to scaling distributed ML systems by teaching efficient parallelization for searching massive state spaces.

## Post-Course Integration Portfolio

* **Target:** Open-source C++ inference engine (e.g., Llama.cpp).
* **Action:** Apply 6.172 profiling techniques to identify a specific bottleneck in C++ execution code or memory access patterns.
