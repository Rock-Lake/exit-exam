An operating system is a program designed to abstract the computer hardware into a more human-usable format by acting as an intermediary. This program executes user programs by controlling the sequence of execution and the allocation of hardware resources.

The smallest form of an operating system is a **Kernel**, any system or application program works atop the kernel. This kernel is stored in a ROM or EEPROM(Electronic Erasable Programmable Read-Only Memory) and packaged with programs that initialize all aspects of the system called **bootstrap program**.

Since all hardware are limited in their resources, to efficiently run programs, the processor **interrupts** the program by suspending the program momentarily. This is usually done by the **Interrupt handler** when there are other instructions while an I/O (Input/Output) operation is in progress and will interrupt again when its' has finished the operation.

**Interrupt handler** is a part of an operating system that determines the nature of an interrupt through an **interrupt vector** which contains the addresses of all the service routines. Interrupt handlers can handle one interrupt at a time to stop a lost interrupt. 

A software generated interrupt caused by an error/user request is called a **trap**. 

Another method for increasing CPU efficiency is **multi-programming**; organizing jobs(code and data) so that the CPU always has a job selected by the **job scheduler** to execute. If the job has to wait for some thing or other, the OS switches to another job. 

**Time-sharing(multitasking)** is an extension of multi-programming in which the CPU executes jobs by switching among them 