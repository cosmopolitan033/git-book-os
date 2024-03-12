# CPU Scheduling

### Introduction to CPU Scheduling
- **Keywords:** CPU scheduling, scheduling policies, operations management, efficiency.
- **Details:** Sets the stage for exploring high-level scheduling policies that determine how and when processes access the CPU. It notes that the origins of scheduling predate computer systems, with early approaches borrowed from operations management.

### Workload Assumptions
- **Keywords:** Simplifying assumptions, unrealistic workload conditions.
- **Details:** Discusses initial simplifying assumptions about the workload, such as uniform job runtimes and simultaneous job arrivals, acknowledging these assumptions are mostly unrealistic but serve as a starting point for developing scheduling policies.

### Scheduling Metrics
- **Keywords:** Turnaround time, scheduling metric, performance measurement.
- **Details:** Introduces turnaround time as a primary metric for evaluating scheduling policies, defined as the difference between job completion and arrival times. This metric helps compare the effectiveness of different scheduling approaches.

### First In, First Out (FIFO)
- **Keywords:** FIFO, FCFS, simplicity, average turnaround time.
- **Details:** Describes FIFO (First In, First Out) or FCFS (First Come, First Served) scheduling, emphasizing its simplicity and how it can work well under the initial unrealistic assumptions, but may lead to suboptimal performance when job lengths vary.

### Shortest Job First (SJF)
- **Keywords:** SJF, job length, optimal scheduling.
- **Details:** Introduces Shortest Job First (SJF) scheduling, which prioritizes jobs based on their length, aiming to minimize average turnaround time. It highlights SJF's theoretical optimality under certain conditions but acknowledges the challenge of not knowing job lengths in advance.

### Shortest Time-to-Completion First (STCF)
- **Keywords:** STCF, preemptive SJF, optimal response time.
- **Details:** Explains Shortest Time-to-Completion First (STCF), a preemptive version of SJF that can improve average turnaround time by allowing the scheduler to preempt longer jobs in favor of shorter ones newly arriving in the system.

### Response Time and Round Robin (RR)
- **Keywords:** Response time, RR, time slice, interactivity.
- **Details:** Discusses the importance of response time, especially for interactive systems, and introduces Round Robin (RR) scheduling as a method that optimizes for lower response times by allocating a fixed time slice to each job in a cyclic order.

### Incorporating I/O and Overcoming Unknown Job Lengths
- **Keywords:** I/O operations, STCF adjustments, predictive scheduling.
- **Details:** Addresses how I/O operations and the unpredictability of job lengths affect scheduling. It suggests approaches for incorporating I/O into scheduling decisions and hints at using historical data to predict job behaviors without exact knowledge of job lengths.

### Summary and Next Steps
- **Keywords:** Scheduling trade-offs, performance vs. fairness, MLFQ.
