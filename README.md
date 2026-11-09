# cuda-simd-axpy

Group 6 Members:
- Gabrielle Joei V. Bactong
- Catherine Gunita
- Shirley Lobo
- Diane Benedict Panganiban

## Project Specifications
The kernel is to perform vector AXPY on vectors $A$ and $B$, placing the result in vector $Z$.

**Input**: Scalar variable $n$ (integer) contains the length of the vector; scalar variable $x$ (single-precision float). Vectors $A$
and $R$ are single-precision floats.

**Process**: $Z_i = a •X; + Y;$ for $i = 0,1,...,n - 1$

**Output**: store the result in vector $Z$. Display the execution time. the first 5. and the last 5 elements of vector $Z$ for verification across all 4 kernels.

**Variants**: (1) a C/C++ program version (2) a CUDA program version using a grid-stride loop without prefetch and without mem advise (3) a CUDA program version using a grid-stride loop with prefetching but without page creation and without mem advise (4) a CUDA program version using a grid-stride loop with prefetch, with page creation but without mem advise (5) a CUDA program version using a grid-stride loop with prefetch, with page creation and with mem advise. For each kernel, execute at least 30 times.


## i) Screenshot of program output with execution time for all cases
**SIMD**

![SIMD 2^20](image/SIMD1.png)

Figure 1. SIMD 2^20

![SIMD 2^24](image/SIMD2.png)

Figure 2. SIMD 2^24

![SIMD 2^27](image/SIMD3.png)

Figure 3. SIMD 2^27

**C Kernel Output**

![C_kernel output](image/image0.jpeg)

Figure 4. C kernel output

**CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise**

![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^20)](image/image5_20_1.jpeg)

Figure 5. CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Array Size: 2^20, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^24)](image/image1.jpeg)

Figure 6. CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Array Size: 2^24, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^27)](image/image9_27_1.jpeg)

Figure 7. CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Array Size: 2^27, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Boundary)](image/image13_boundary_1.jpeg)

Figure 8. CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Array Size: 1003, Block Size: 256, 512, 1024) 


**CUDA with Grid-stride Loop and prefetch and without page creation and memory advise**

![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^20)](image/image6_20_2.jpeg)

Figure 9. CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Array Size: 2^20, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^24)](image/image2.jpeg)

Figure 10. CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Array Size: 2^24, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^27)](image/image10_27_2.jpeg)

Figure 11. CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Array Size: 2^27, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Boundary)](image/image14_boundary_2.jpeg)

Figure 12. CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Array Size: 1003, Block Size: 256, 512, 1024) 


**CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise**

![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^20)](image/image7_20_3.jpeg)

Figure 13. CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Array Size: 2^20, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^24)](image/image3.jpeg)

Figure 14. CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Array Size: 2^24, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^27)](image/image11_27_3.jpeg)

Figure 15. CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Array Size: 2^27, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Boundary)](image/image15_boundary_3.jpeg)

Figure 16. CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Array Size: 1003, Block Size: 256, 512, 1024) 

**CUDA with Grid-stride Loop, prefetch, page creation, and memory advise**

![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^20)](image/image8_20_4.jpeg)

Figure 17. CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Array Size: 2^20, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^24)](image/image4.jpeg)

Figure 18. CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Array Size: 2^24, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^27)](image/image12_27_4.jpeg)

Figure 19. CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Array Size: 2^27, Block Size: 256, 512, 1024) 

![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Boundary)](image/image16_boundary_4.jpeg)

Figure 20. CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Array Size: 1003, Block Size: 256, 512, 1024) 

## ii) Comparative Table

![Comparative Table](images/comparative_table.png)

Figure 18. Comparative Table of Average Execution Time with size: 2^20, 2^26, and 2^27


## ii.a) Speedup comparisons of versions against C

![Speedup comparisons of versions against C](images/SpeedUp.png)

Figure 19. Speed Up Comparisons of versions against C 

## vi) Difference between SIMT and SIMD in handling Parallelism (WIP)

SIMD (Single Instruction, Multiple Data) and SIMT (Single Instruction, Multiple Threads) are both approaches to parallel computing, but they differ in how instructions and data are processed.

SIMD executes a single instruction on multiple data elements simultaneously using vector registers. For example, a 128-bit XMM register can process four single-precision floating-point values, while a 256-bit YMM register can process eight. This allows CPUs to perform the same operation on multiple elements using fewer instructions compared to scalar processing (Intel, n.d.). In our project, we implemented a conventional C version of the AXPY operation as the CPU baseline. Although the compiler may automatically vectorize the loop, explicit SIMD instructions such as AVX2 were not implemented in the notebook.

SIMT, on the other hand, executes multiple threads that follow the same instruction sequence on different data elements. In our CUDA implementation, each GPU thread processes vector elements independently using its assigned thread index. Threads are organized into blocks within a grid, allowing the GPU to execute many threads concurrently. Threads within a warp generally execute instructions together, although different execution paths may occur when branching is involved (NVIDIA, n.d.-a).

We implemented a grid-stride loop in our CUDA kernels to support vector sizes larger than the total number of threads launched in the grid. Each thread calculates its starting index using `blockIdx.x`, `blockDim.x`, and `threadIdx.x`, then advances by the total number of threads in the grid until all assigned elements have been processed. This allows each thread to process multiple vector elements without requiring a separate thread for every element.

In our AXPY operation, both the CPU and GPU implementations perform the same computation:

`Z[i] = a * X[i] + Y[i]`

However, their execution differs. The CPU baseline processes the elements through a conventional C loop, which may be automatically vectorized by the compiler. The CUDA implementation explicitly distributes the computation across multiple GPU threads using SIMT.

#### Advantages and Disadvantages in Our Use Case

| Approach | Advantages | Disadvantages |
| --- | --- | --- |
| **SIMD** | Processes multiple data elements per vector instruction, making it efficient for repetitive numerical computations. Can improve CPU performance without requiring GPU memory management or kernel launches. | Performance depends on the CPU instruction set, vector width, and compiler optimization. Explicit SIMD programming requires consideration of data alignment, vectorization, and remaining elements. |
| **SIMT** | Supports large numbers of concurrent GPU threads, making it suitable for highly parallel workloads. Grid-stride loops allow flexible processing of different vector sizes. CUDA also provides memory-management techniques such as prefetching and memory advice. | Requires GPU kernel launches and memory management. Data migration between CPU and GPU memory may introduce overhead. Performance can also depend on block configuration, memory access patterns, and GPU hardware. |

These differences are consistent with Intel's description of SIMD vector instructions and NVIDIA's explanation of GPU thread execution and memory optimization (Intel, n.d.; NVIDIA, n.d.-a; NVIDIA, n.d.-b).

#### Observations from the AXPY Implementation

Based on our implementation, the CPU baseline and CUDA SIMT approach demonstrate two different ways of executing the same AXPY computation. The CPU implementation uses a sequentially expressed C loop, while the CUDA implementation distributes the workload across multiple GPU threads.

Our CUDA implementation also explores different memory-management strategies through four kernel variants: baseline Unified Memory, memory prefetching, prefetching with page creation, and prefetching with page creation and memory advice. These variants allow us to investigate how data placement and memory migration may affect GPU execution.

Additionally, the CUDA implementation uses grid-stride loops and experiments with different grid configurations, including 256, 512, and 1024 blocks. This demonstrates how thread organization and memory-management strategies can be adjusted without changing the underlying AXPY computation.

Overall, SIMD and SIMT both provide ways to exploit data parallelism. SIMD achieves this through vector instructions operating on multiple data elements, while SIMT distributes operations across multiple threads. In our project, the conventional C implementation serves as the CPU baseline, while CUDA demonstrates explicit SIMT parallelism and provides opportunities to investigate GPU memory-management optimizations.

## AI USAGE DECLARATION 
Generative AI was not used in the development of the kernels outlined in this project.
