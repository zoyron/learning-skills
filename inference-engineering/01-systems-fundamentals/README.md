# Phase 1: Systems Foundations (The "Bare Metal" Manual)

**Goal:** Master the movement of data between CPU, RAM, and GPU. If you don't understand the "cost" of a memory fetch, you can't optimize inference.

## The Detailed Steps
- **Memory Alignment & Cache Locality:** Learn to write cache-friendly C++. Study Data-Oriented Design (DOD). Avoid "Pointer Chasing" (linked lists) which causes cache misses.
- **Concurrency & Synchronization:** Master Atomics, Memory Barriers, and Lock-Free Programming. In HFT, we avoid `std::mutex` because it’s too slow; we use Spinlocks or SPSC Queues.
- **The CUDA Execution Model:** Understand Warps, Thread Blocks, and Grid dimensions. Learn to use Shared Memory (SRAM) as a manual cache to avoid hitting the slower Global Memory (VRAM).
- **SIMD & Vectorization:** Learn how to use AVX-512 or ARM Neon instructions to perform multiple operations per clock cycle on the CPU before offloading to the GPU.

## Resources & Books

For convenience, key papers and documentation have been downloaded to the **[resources/](./resources/)** directory. See **[Resources.md](./resources/Resources.md)** for a full index.

- **[NEW] [Local Resource Index](./resources/Resources.md)**
- **Book:** *C++20 in Detail* by Bartłomiej Filipek. [Purchase](https://leanpub.com/cpp20indetail)
- **Book:** *Professional CUDA C Programming* by John Cheng. [Purchase](https://www.wiley.com/en-us/Professional+CUDA+C+Programming-p-9781118739327)
- **Paper:** *What Every Programmer Should Know About Memory* by Ulrich Drepper. [Local PDF](./resources/what_every_programmer_should_know_about_memory.pdf)
- **Documentation:** NVIDIA CUDA C++ Programming Guide. [Local PDF](./resources/cuda_c_programming_guide.pdf)

- **Course:** High Performance Computing (HPC) Specialization via Coursera or the IIT Delhi HPC open modules.


## HFT Pro-Tip
Use a profiler like NVIDIA Nsight Systems. If your "Compute Utilization" is high but your "Memory Bandwidth" is low, your kernels are starving. Fix the data path before you touch the math.
