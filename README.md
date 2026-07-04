# Parallel Bitonic Sort using CUDA

## Project Description
The main goal is to study the **Bitonic Sort algorithm** by implementing it in two ways:
1.  **Sequential Version:** CPU-based implementation using C++.
2.  **Parallel Version:** GPU-based implementation using CUDA.

We compare the performance of both implementations to evaluate the speedup achieved through parallel processing.

## What the Program Does
### Input
- Randomly generated integer arrays with varying sizes:
  - **Small:** $2^{10}$ (1,024 elements)
  - **Medium:** $2^{15}$ (32,768 elements)
  - **Large:** $2^{20}$ (1,048,576 elements)
- User-defined input (used for demonstration and testing).

### Output
- A fully sorted array in ascending or descending order.
- Execution time comparison for both CPU and GPU.
- Performance analysis and speedup metrics.

## Implementation Details
The project includes two main implementations:

* **Sequential Implementation:**
    * Written in **C++**.
    * Used as a baseline to measure performance.

* **Parallel Implementation:**
    * Written in **CUDA C++**.
    * Runs on an **NVIDIA GPU** (Tested on Tesla T4 via Google Colab).
    * Designed to exploit massive GPU parallelism.

## Key Techniques Used
* **Thread-Level Parallelism:** Compare-and-swap operations are executed concurrently by thousands of GPU threads.
* **Bitonic Sorting Network:** A deterministic sorting network structure suitable for SIMT architecture.
* **Scalability Analysis:** Benchmarking performance across exponential dataset sizes to identify hardware bottlenecks.

## Results
The CUDA version achieved a **speedup of up to 300×** for the largest dataset ($2^{20}$ elements).

**Execution Time for 1 million elements:**
* **GPU:** ~6 ms
* **CPU:** ~1800 ms

> These results demonstrate the significant efficiency of GPU-based parallel processing for large-scale sorting tasks.

## Contributors
This project was a collaborative team effort by:
- Najd Aljarba
- Lama Alarfaj
- Athoog Alsuhaibany
- Ghadah Alammar
- Razan Rashid
