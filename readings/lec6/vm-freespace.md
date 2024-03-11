# VM Free Space Management

### Introduction to Free-Space Management
- **Keywords:** Free-space management, external fragmentation, malloc, free.
- **Details:** Discusses the problem of managing free memory space, especially in the context of variable-sized units. The document outlines the challenge of external fragmentation, where free space is divided into non-contiguous chunks, making it difficult to satisfy memory requests even when there's enough total free space.

### Managing Free Space
- **Keywords:** Splitting, coalescing, free list, heap management.
- **Details:** Introduces basic mechanisms used in memory allocation, such as splitting (dividing free chunks to satisfy requests) and coalescing (merging adjacent free chunks). These strategies aim to optimize the use of space and reduce fragmentation.

### Allocation Strategies
- **Keywords:** Best fit, worst fit, first fit, next fit.
- **Details:** Explores different strategies for selecting free chunks during memory allocation:
  - **Best Fit:** Chooses the smallest chunk that is large enough to satisfy a request, minimizing wasted space but potentially expensive due to the need to search the entire free list.
  - **Worst Fit:** Selects the largest chunk, with the goal of leaving larger remaining chunks, but can lead to excessive fragmentation.
  - **First Fit:** Allocates the first chunk that is large enough, reducing search time compared to best and worst fit but may increase fragmentation at the beginning of the free list.
  - **Next Fit:** Similar to first fit but continues searching from the point of the last allocation, aiming to distribute fragmentation more evenly.

### Low-Level Mechanisms
- **Keywords:** Headers, size tracking, embedding free lists.
- **Details:** Details the use of headers for tracking the size of allocated regions, a crucial feature since the `free()` function doesn't take a size parameter. Discusses how allocators embed free lists within the free space itself, utilizing the memory being managed to track available chunks.

### Growing the Heap
- **Keywords:** Heap expansion, `sbrk`, system calls.
- **Details:** Addresses the allocator's response when running out of space, typically by requesting more memory from the operating system through system calls like `sbrk`, to expand the heap.

### Advanced Management Techniques
- **Keywords:** Segregated lists, buddy allocation, slab allocation.
- **Details:** Introduces advanced techniques for managing free space:
  - **Segregated Lists:** Uses separate lists for common request sizes to quickly satisfy allocations with minimal fragmentation.
  - **Buddy Allocation:** Splits memory into blocks sized as powers of two, simplifying coalescing by pairing adjacent blocks of the same size.
  - **Slab Allocation:** Pre-allocates blocks for commonly sized objects, keeping them initialized for quicker reuse.
