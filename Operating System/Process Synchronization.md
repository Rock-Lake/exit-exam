[[Process#^c35ee6|Cooperating processes]] can execute concurrently, utilizing different resources. However, how do these processes work if they're using common resources concurrently without resulting in data inconsistency? This situation is called a **race condition**.

Solving the race condition in sync requires to isolate the **critical section**, i.e, the part that shares resources of a process and enforce a protocol so that the OS can *enter* and *exit* the critical section of the processes in sequence.

Other solutions to the **critical section problem** requires the following guarantees:
- **Mutual exclusion** - Only one process can execute their critical section
- **Progress** - if there's no process that entered its critical section and there's one that wants to, it won't wait forever.
- **Bounded waiting** - there must be a fixed number of times for processes to wait for their request to enter their critical section
- **No preemption** - processes running in [[Operating Systems#^f4a871|kernel mode]] are [[CPU Scheduling#^677fab|preemptive]]

Several solutions to the critical solutions problem have been made, they are:
- **Peterson's solution** - uses an integer *turn* variable to indicate whose turn to enter the critical section and a flag to verify the turn. The turn will point the next process and the flag will be *false* at the end of the critical section.
- **Semaphores** - use a variable **S** to indicate the status of the process and 2 functions, wait() and signal() to decrement/increment the value. If wait() is used then S is decreased into negative and process is put into wait queue. 