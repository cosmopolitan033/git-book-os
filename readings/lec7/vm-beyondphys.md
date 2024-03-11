# Beyond Physical Memory

### Introduction to Swapping
- **Keywords:** Swap space, hard disk drives, SSDs, large virtual memory, multiprogramming.
- **Details:** Discusses the necessity of using secondary storage devices like hard disk drives or SSDs as swap space to support large address spaces and multiple concurrently running processes. This approach allows the operating system to move parts of the address space not currently in demand to swap space, effectively managing memory resources and supporting the illusion of a large virtual memory.

### Swap Space Allocation
- **Keywords:** Swap space, disk, page swapping, process management.
- **Details:** Introduces the concept of swap space on the disk where the operating system can store pages that are not actively used in physical memory. This section explains how swap space enables the operating system to manage memory more flexibly by swapping pages in and out as needed.

### The Present Bit and Page Faults
- **Keywords:** Present bit, page table entry, page fault handler, hardware vs. software TLB management.
- **Details:** Describes the role of the present bit in page table entries to indicate whether a page is in physical memory. If a page is not present (the present bit is set to zero), accessing the page triggers a page fault, prompting the operating system's page-fault handler to load the page into memory from swap space.

### Handling Page Faults
- **Keywords:** Page fault handling, TLB misses, disk I/O, swap space management.
- **Details:** Explores the process of handling page faults, including the steps the operating system takes to locate the faulting page in swap space, initiate disk I/O to load the page into memory, and update the page table and TLB accordingly. This section emphasizes the efficiency of managing memory access and the role of the operating system in mitigating the performance impact of page faults.

### Page Replacement Policy
- **Keywords:** Page replacement, eviction algorithms, performance implications.
- **Details:** Discusses the importance of an effective page replacement policy to determine which pages to evict from physical memory to make space for new pages. It highlights the performance implications of different replacement strategies and the need for algorithms that minimize the impact on application performance.

### Swap Space Management
- **Keywords:** Swap daemon, high watermark, low watermark, disk I/O optimization.
- **Details:** Covers the strategies for managing swap space, including the use of a background swap daemon that frees up physical memory based on predefined high and low watermarks. It also touches on the potential for optimizing disk I/O operations by clustering page writes to swap space.

### Summary
- **Keywords:** Virtual memory extension, swapping, page replacement, operating system management.
