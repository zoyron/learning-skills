# Phase 1: Systems Foundations (The "Bare Metal" Manual)

**Goal:** Master the movement of data between CPU, RAM, and GPU. If you don't understand the "cost" of a memory fetch, you can't optimize inference.

## The Detailed Steps
- **Memory Alignment & Cache Locality:** Learn to write cache-friendly C++. Study Data-Oriented Design (DOD). Avoid "Pointer Chasing" (linked lists) which causes cache misses.
- **Concurrency & Synchronization:** Master Atomics, Memory Barriers, and Lock-Free Programming. In HFT, we avoid `std::mutex` because it’s too slow; we use Spinlocks or SPSC Queues.
- **The CUDA Execution Model:** Understand Warps, Thread Blocks, and Grid dimensions. Learn to use Shared Memory (SRAM) as a manual cache to avoid hitting the slower Global Memory (VRAM).
- **SIMD & Vectorization:** Learn how to use AVX-512 or ARM Neon instructions to perform multiple operations per clock cycle on the CPU before offloading to the GPU.

## Resources & Books
- **Book:** *C++20 in Detail* by Bartłomiej Filipek (Updated for C++23/26 features).
- **Book:** *Professional CUDA C Programming* by John Cheng (Reference the CUDA 13.x documentation for the latest Blackwell/Hopper features).
- **Documentation:** NVIDIA CUDA C++ Programming Guide (Release 13.2).
- **Course:** High Performance Computing (HPC) Specialization via Coursera or the IIT Delhi HPC open modules.
- **Paper:** *What Every Programmer Should Know About Memory* by Ulrich Drepper (The "Bible" of systems engineering).

## HFT Pro-Tip
Use a profiler like NVIDIA Nsight Systems. If your "Compute Utilization" is high but your "Memory Bandwidth" is low, your kernels are starving. Fix the data path before you touch the math.
