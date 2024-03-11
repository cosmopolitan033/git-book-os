# Paging

### Introduction to Paging
- **Keywords:** Virtual memory, segmentation, paging, fragmentation, Atlas system.
- **Details:** The document starts by discussing the drawbacks of segmentation in memory management, such as external fragmentation, and introduces paging as a more efficient alternative that divides memory into fixed-sized pages to avoid these issues.

### Basics of Paging
- **Keywords:** Pages, page frames, virtual address space, physical memory, address translation.
- **Details:** Paging is described as dividing both the virtual address space and physical memory into fixed-sized units called pages and page frames, respectively. This approach simplifies memory management and supports the efficient virtualization of memory by mapping virtual pages to physical page frames.

### Advantages of Paging
- **Keywords:** Flexibility, free-space management, page table, address space abstraction.
- **Details:** Highlights the advantages of paging, including flexibility in managing address spaces and simplicity in free-space management. The role of the page table in storing address translations is emphasized as crucial for understanding where virtual pages reside in physical memory.

### Address Translation Mechanism
- **Keywords:** Virtual page number (VPN), physical frame number (PFN), offset, page table, address translation.
- **Details:** Explains the process of translating virtual addresses to physical addresses using a page table. The virtual address is split into a VPN and an offset; the VPN is used to index the page table and find the corresponding PFN, which, combined with the offset, forms the physical address.

### Storing Page Tables
- **Keywords:** Linear page table, memory requirement, 32-bit and 64-bit address spaces.
- **Details:** Discusses the storage of page tables, typically in physical memory, and the implications for memory usage. The size of page tables can be substantial, especially for large address spaces, necessitating efficient management and storage solutions.

### Page Table Contents
- **Keywords:** Valid bit, protection bits, present bit, dirty bit, reference bit.
- **Details:** Details the contents of a page table entry (PTE), including bits for validity, protection (read/write/execute permissions), presence in memory, modification (dirty bit), and access (reference bit), illustrating how these control access to and management of memory pages.

### Page Table Structure
- **Keywords:** Data structures, linear page table, mapping virtual to physical addresses.
- **Details:** Introduces the linear page table as a simple array-based structure for mapping virtual page numbers to physical frame numbers, with each entry containing the physical address translation and additional control bits.

### Paging Performance Concerns
- **Keywords:** Memory accesses, page table fetch, physical address computation, system performance.
