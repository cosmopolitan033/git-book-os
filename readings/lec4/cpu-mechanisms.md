# CPU Mechanisms

### Limited Direct Execution and its Challenges
- **Keywords:** Limited direct execution, performance, control, virtualization.
- **Details:** Limited direct execution is introduced as a strategy for CPU virtualization, aiming to run processes directly on the CPU while maintaining system control. The document outlines the challenges of ensuring efficient operation without sacrificing control over resources.

### Basic Technique: Limited Direct Execution
- **Keywords:** Direct execution, process creation, memory allocation, execution control.
- **Details:** The process of starting a program involves creating a process entry, allocating memory, loading the program into memory, and initiating execution. Despite its efficiency, direct execution raises issues related to unrestricted program actions and the OS's ability to retain control.

### Problem #1: Restricted Operations
- **Keywords:** Restricted operations, user mode, kernel mode, system calls.
- **Details:** Discusses the problem of allowing processes to perform restricted operations like I/O requests, proposing user mode and kernel mode to differentiate between unrestricted OS operations and restricted user process operations.

### Problem #2: Switching Between Processes
- **Keywords:** Process switching, cooperative approach, timer interrupt.
- **Details:** Addresses how the OS switches between processes, either waiting for system calls (cooperative approach) or using timer interrupts (non-cooperative approach) to forcibly regain control and manage CPU scheduling.

### Saving and Restoring Context
- **Keywords:** Context switch, register saving, scheduler decisions.
- **Details:** Explores the context switch mechanism, where the OS saves the current process's state and restores another's, enabling smooth transitions between processes as part of CPU scheduling.

### Execution Modes and System Calls
- **Keywords:** Execution modes, trap instruction, system call handling.
- **Details:** The document explains execution modes (user and kernel) and the role of system calls and trap instructions in transitioning between these modes while ensuring controlled access to system resources.

### Summary and Concluding Thoughts
- **Keywords:** CPU virtualization, limited direct execution benefits, process management.
