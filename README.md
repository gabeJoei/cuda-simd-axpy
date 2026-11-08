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

**C Kernel Output**
![C_kernel output](images/image0.jpeg)

**CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise**
**2^20**
![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^20)](images/image1.jpeg)
**2^26**
![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^26)](images/image2.jpeg)
**2^27**
![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (2^27)](images/image3.jpeg)
**Boundary Check**
![CUDA with Grid-stride Loop and without prefetch, page creation, and memory advise (Boundary)](images/image4.jpeg)

**CUDA with Grid-stride Loop and prefetch and without page creation and memory advise**
**2^20**
![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^20)](images/image5.jpeg)
**2^26**
![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^26)](images/image6.jpeg)
**2^27**
![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (2^27)](images/image7.jpeg)
**Boundary Check**
![CUDA with Grid-stride Loop and prefetch and without page creation and memory advise (Boundary)](images/image8.jpeg)

**CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise**
**2^20**
![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^20)](images/image9.jpeg)
**2^26**
![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^26)](images/image10.jpeg)
**2^27**
![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (2^27)](images/image11.jpeg)
**Boundary Check**
![CUDA with Grid-stride Loop, prefetch, and page creation and without memory advise (Boundary)](images/image12.jpeg)

**CUDA with Grid-stride Loop, prefetch, page creation, and memory advise**
**2^20**
![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^20)](images/image13.jpeg)
**2^26**
![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^26)](images/image14.jpeg)
**2^27**
![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (2^27)](images/image15.jpeg)
**Boundary Check**
![CUDA with Grid-stride Loop, prefetch, page creation, and memory advise (Boundary)](images/image16.jpeg)
## AI USAGE DECLARATION 
Generative AI was not used in the development of the kernels outlined in this project.
