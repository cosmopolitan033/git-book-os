# CPU API

### The `fork()` System Call
- **Keywords:** Process creation, PID, child and parent processes, return values.
- **Details:** `fork()` creates a new process by duplicating the calling process. The new process, called the child, is an almost exact copy of the parent process, including its code, data, and open files. The primary distinction is in the return value: the parent gets the PID of the child, while the child receives 0.

### The `wait()` System Call
- **Keywords:** Synchronization, parent and child processes, execution completion.
- **Details:** `wait()` allows a parent process to delay its execution until its child finishes executing. By using `wait()`, the parent ensures it can perform cleanup or further actions only after the child's completion, thus enforcing a specific order of execution.

### The `exec()` System Call
- **Keywords:** Program execution, replacing process image, command-line arguments.
- **Details:** `exec()` replaces the current process image with a new program image, effectively transforming the executing program. This call is useful when a process needs to run a different program. Unlike `fork()`, `exec()` does not create a new process; instead, it transforms the existing process into a new program.

### Process API in Practice
- **Keywords:** UNIX shell, input/output redirection, pipes, environment manipulation.
- **Details:** The separation of `fork()` and `exec()` is crucial for UNIX shells, enabling features like I/O redirection and pipes without altering the programs being run. The shell uses `fork()` to create a new process, potentially manipulates the environment or redirects I/O, and then uses `exec()` to execute the desired command.
