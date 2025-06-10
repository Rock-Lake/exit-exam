An operating system interactivity depends on its ability to switch among processes. This requires processes to be assigned to run on available CPUs using a **scheduling algorithm** to queue processes for selection.

Processes usually alternate between bursts of CPU execution and I/O operations.

The scheduling algorithm is implemented on **schedulers**, kernel programs that selects processes from the [[Process#^b6d1d5|ready]] queue and allocate into the CPU. Depending on the range of time the scheduler controls, there are 3 types:
- **Short-term scheduler** - selects jobs from ready queue to CPU
- **Medium-term scheduler** - involved in [[swapping]], moves processes from memory to disk
- **Long-term scheduler** - balances processes with large CPU bursts and large I/O bursts.

Schedulers can be either be:
- **Preemptive** - can remove ongoing processes from CPU ^677fab
- **Non-preemptive** - waits for process to terminate/wait before switching with other processes

