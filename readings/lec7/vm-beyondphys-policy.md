# Beyond Physical Memory - Policy

### The Crux of Page Eviction Decisions
- **Keywords:** Memory pressure, page eviction, replacement policy.
- **Details:** Explores the dilemma of choosing which pages to evict when free memory is low, a decision governed by the replacement policy. The document sets the stage for discussing how to optimize this process to enhance system performance.

### Cache Management and Goals
- **Keywords:** Cache misses, average memory access time (AMAT), hit and miss rates.
- **Details:** Introduces the concept of main memory as a cache for virtual pages, aiming to minimize cache misses to reduce the average memory access time, thereby improving overall system efficiency.

### The Optimal Replacement Policy
- **Keywords:** Belady's optimal policy, future knowledge, MIN algorithm.
- **Details:** Discusses Belady's theoretical optimal replacement policy, which minimizes cache misses by evicting the page that won't be used for the longest time in the future, albeit impractical for real-world implementation due to its requirement for future knowledge.

### Simple Policies: FIFO and Random
- **Keywords:** FIFO (First-In, First-Out), random replacement, policy effectiveness.
- **Details:** Evaluates simple replacement policies like FIFO, where pages are evicted in the order they were brought into memory, and random replacement, highlighting their simplicity but limited effectiveness in reducing cache misses.

### History-Based Policies: LRU
- **Keywords:** Least Recently Used (LRU), recency of access, principle of locality.
- **Details:** Introduces LRU and similar history-based policies that use past page access information to predict future accesses, aiming to keep frequently or recently used pages in memory to improve hit rates.

### Implementing LRU: Challenges and Approximations
- **Keywords:** Hardware support, use bit, clock algorithm, dirty pages.
- **Details:** Discusses the implementation challenges of perfect LRU due to the overhead of tracking page accesses. Presents the clock algorithm as a practical approximation of LRU, using a use bit for each page and additional considerations for dirty (modified) pages to decide on evictions.

### Workload Examples and Policy Evaluation
- **Keywords:** No-locality, 80-20 workload, looping-sequential workload.
- **Details:** Analyzes different workloads to compare the effectiveness of various replacement policies, demonstrating how policies like LRU can be more effective than FIFO or random in workloads with certain patterns of locality.

### Summary and Future Directions
- **Keywords:** Page replacement algorithms, memory-access vs. disk-access times, storage technology impact.
