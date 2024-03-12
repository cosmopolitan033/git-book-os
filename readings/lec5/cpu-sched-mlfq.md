# CPU Scheduling - MLFQ

### Introduction to MLFQ
- **Keywords:** Multi-Level Feedback Queue, turnaround time, response time, Corbato et al., Compatible Time-Sharing System (CTSS).
- **Details:** Introduces MLFQ as a solution to optimize both turnaround and response times by adjusting job priorities based on their behavior. Originally developed for the CTSS, MLFQ has evolved into a fundamental scheduling approach in modern operating systems.

### MLFQ: Basic Rules and Design
- **Keywords:** Priority levels, queues, Round Robin (RR), dynamic priority adjustment.
- **Details:** Describes MLFQ's structure of multiple queues with different priority levels, where jobs are scheduled primarily based on their priority. The document outlines basic rules for job execution within and across these priority levels, emphasizing the dynamic adjustment of priorities based on job behavior.

### Learning from History
- **Keywords:** Job behavior, interactive jobs, CPU-bound jobs, adaptability.
- **Details:** MLFQ learns from the execution history of jobs, adjusting priorities to favor short, interactive jobs for responsiveness and managing long, CPU-bound jobs to ensure fairness and efficient CPU utilization.

### Priority Adjustment Mechanisms
- **Keywords:** Time slices, priority reduction, allotment, interactive vs. CPU-bound jobs.
- **Details:** Discusses the mechanisms for adjusting job priorities, including the use of time slices and allotments to demote or maintain job priorities. This adaptive strategy aims to differentiate between interactive and CPU-bound jobs, treating them accordingly.

### Challenges and Refinements
- **Keywords:** Starvation, gaming the scheduler, priority boost, better accounting.
- **Details:** Addresses challenges such as starvation and potential gaming by smart users. It introduces solutions like periodic priority boosts to prevent starvation and refined accounting rules to counteract gaming, ensuring a more balanced and fair CPU allocation among jobs.

### Tuning and Practical Considerations
- **Keywords:** Scheduler parameterization, queue numbers, time slice lengths, workload adaptation.
- **Details:** Explores practical considerations for tuning MLFQ parameters, such as the number of queues, time slice lengths per queue, and the frequency of priority boosts. It acknowledges the difficulty in setting these parameters optimally, suggesting the need for experience and workload-specific adjustments.

### Summary of MLFQ
- **Keywords:** Feedback-based scheduling, performance optimization, fairness, historical behavior.
