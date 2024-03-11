# VM API

### Types of Memory
- **Keywords:** Stack memory, heap memory, automatic memory, dynamic allocation.
- **Details:** Distinguishes between stack (automatic) memory, managed implicitly by the compiler, and heap memory, where allocation and deallocation are explicitly handled by the programmer.

### The `malloc()` Call
- **Keywords:** `malloc()`, dynamic allocation, heap memory, size allocation.
- **Details:** Introduces `malloc()` as a fundamental call for allocating memory on the heap, requiring programmers to specify the desired allocation size and manage the allocated memory.

### Tips for Using `sizeof()` and `malloc()`
- **Keywords:** `sizeof()` operator, dynamic memory allocation, correct usage.
- **Details:** Offers tips on correctly using the `sizeof()` operator with `malloc()` to allocate memory of the appropriate size, emphasizing the importance of accounting for the right data types and avoiding common mistakes.

### The `free()` Call
- **Keywords:** `free()`, deallocating memory, heap management.
- **Details:** Discusses the use of `free()` to deallocate memory previously allocated with `malloc()`, highlighting the importance of proper memory management to prevent leaks.

### Common Errors in Memory Management
- **Keywords:** Allocation errors, forgetting to free memory, buffer overflow.
- **Details:** Identifies common memory management errors, such as failing to allocate memory, not allocating enough memory, forgetting to initialize allocated memory, and incorrectly freeing memory.

### Supporting Calls and Tools
- **Keywords:** `calloc()`, `realloc()`, memory initialization, resizing memory.
- **Details:** Introduces additional memory allocation functions like `calloc()` for allocation and initialization, and `realloc()` for resizing previously allocated memory blocks.

### Underlying OS Support
- **Keywords:** `brk`, `sbrk`, memory allocation library, system calls.
- **Details:** Explains the underlying system calls (`brk` and `sbrk`) that support memory allocation libraries, cautioning against their direct use in favor of higher-level library functions.

### Tools for Memory Debugging
- **Keywords:** `gdb`, `valgrind`, memory leak detection, debugging practices.
- **Details:** Recommends using debugging tools like `gdb` for general debugging and `valgrind` for detecting memory leaks and other memory-related issues, stressing the importance of familiarizing oneself with these tools.

### Summary
- **Keywords:** Memory API, allocation best practices, debugging and validation tools.
