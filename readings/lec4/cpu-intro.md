# CPU Introduction

### The Process Abstraction
- **Keywords:** Process definition, running program, operating system's role.
- **Details:** A process is informally defined as a running program. The document emphasizes that while a program is a static set of instructions, it's the operating system that transforms it into a dynamic process, executing on the CPU and performing tasks.

### Multiprogramming and Time Sharing
- **Keywords:** Concurrent execution, CPU utilization, illusion of many CPUs.
- **Details:** The ability to run multiple programs simultaneously (multiprogramming) and the development of time-sharing systems are discussed as advancements that improve CPU utilization and user experience by providing the illusion of numerous concurrent processes.

### Virtualizing the CPU
- **Keywords:** Time sharing, virtual CPUs, performance costs.
- **Details:** The document outlines the concept of CPU virtualization, where the operating system shares the CPU among multiple processes by quickly switching between them, giving the impression that each has its own CPU.

### Mechanisms and Policies
- **Keywords:** Low-level machinery, high-level intelligence, scheduling policies.
- **Details:** It differentiates between mechanisms (how functionalities are implemented) and policies (decisions within the OS, such as which process to run next), underlining the importance of both in effective CPU virtualization.

### The Process API
- **Keywords:** Create, destroy, wait, control, status.
- **Details:** Introduces a basic Process API that includes functionalities for creating new processes, destroying processes, waiting for processes to complete, and obtaining process status, illustrating how these actions are fundamental for managing processes in an operating system.

### Process Creation Details
- **Keywords:** Loading program, static data, memory allocation, I/O setup.
- **Details:** Describes the steps involved in creating a process, including loading the program and its data into memory, allocating memory for the stack and heap, and setting up I/O, culminating in the program starting execution at the `main()` function.

### Process States
- **Keywords:** Running, ready, blocked, state transitions.
- **Details:** Explains the various states a process can be in (running, ready, blocked) and how processes transition between these states due to actions like CPU scheduling, I/O operations, and completion of I/O.

### Process Lists and Control Blocks
- **Keywords:** Process list, Process Control Block (PCB), tracking processes.
- **Details:** The document highlights the use of process lists and Process Control Blocks for tracking the state and information of each process in the system, underscoring the organizational aspects of process management.
