An operating system is a program designed to simplify the access of computer hardware to the user. This program executes user programs by controlling the sequence of execution and the allocation of hardware resources.

An operating system is located in the layered structure of a computer system where:
- **Users**, either other machines or people use the computer;
- **Application programs** are executed to solve the user's particular problem;
- **Operating System** manages the use of computer hardware by providing services such as [[Process|program execution]], [[CPU Scheduling|process scheduling]], [[Process Synchronization|process synchronization]], and [[Memory|memory management]] through [[System Calls|system calls]].
- **Hardware**, provides access the computer's resources
## Operating System Structure
Operating systems can be structured into many ways, it can either be a single(monolithic) system or a collection of components called **kernel modules**.

The smallest form of an operating system is a **Kernel**, any system or application program works on top of the kernel. This kernel is stored in a ROM or EEPROM(Electronic Erasable Programmable Read-Only Memory) and packaged with programs that initialize all aspects of the system called **bootstrap program**.

Another method for increasing CPU efficiency is **multi-programming**; organizing jobs(code and data) so that the CPU always has a job selected by the [[CPU Scheduling|job scheduler]] to execute. If the job has to wait for some thing or other, the OS switches to another job. 

**Time-sharing(multitasking)** is an extension of multi-programming in which the CPU executes jobs by switching among them quickly enough to give the illusion of an interactive system.
## Operating System Operations
Since all hardware are limited in their resources, to efficiently run programs, the processor **interrupts** the program by suspending the program momentarily. This is usually done by the **Interrupt handler** when there are other instructions while an I/O (Input/Output) operation is in progress and will interrupt again when its' has finished the operation.

**Interrupt handler** is a part of an operating system that determines the nature of an interrupt through an **interrupt vector** which contains the addresses of all the service routines. Interrupt handlers can handle one interrupt at a time to stop a lost interrupt. 

A software generated interrupt caused by an error/user request is called a **trap**.  ^f5c55f

Modern OS are interrupt driven, meaning the system reacts to processes, else wait for something to happen.

To ensure proper program execution without affecting other processes, a **dual-mode** of operation is used. This separates user processes and kernel processes by attaching a *mode bit* to processes. User processes have mode-bit 1 and kernel processes have mode-bit 0. [[Process|Processes]] that require kernel-level access to computer hardware will use a [[System Calls|system call]] that changes the process' mode-bit using a [[#^f5c55f|trap]]. ^f4a871

## System Programs
Modern systems package OS kernels with other programs, providing an environment for program development and execution. Some are user interfaces to [[System Calls|system calls]], while others are more complex. They can be divided into these categories:
- **File management** - programs to create, delete, copy, rename, print, dump, list, and manipulate files and folders
- **Status information** - programs that request system resources or information, log and store system performance and configuration.
- **File modification** - text editors like notepad, Emacs, nano, vim...
- **Programming language support** - compilers, assemblers, debuggers and interpreters for common programming languages
- **Program loading and execution** - programs that load compiled programs into memory
- **Communications** - connection managers, web browsers, file transfer
- **Background services** - daemons and subsystems.
## Computing Environment
There are many different methods of implementing an operating system. They are:
- **Traditional** - Office computers connected to a network to processes batch requests
- [[Distributed Systems|Distributed]] - a collection of physically separate computers networked to share hardware and software resources
- **Client-Server** - a collection of networked computers that are either resource providers or interfaces to access services and files.
- **Peer-to-Peer(P2P)** - a [[Distributed Systems|distributed system model]], the nodes in the network either advertise their services using a *discovery protocol* or register their services to a central lookup table for easy navigation of the network.
- **Virtualization** - operating systems run as applications within other operating systems. 
- **Cloud** - provides computing services across a network. It provides the computing resources as virtual machines in the servers.
- **Real-Time Embedded Systems** - designed for specific tasks, these system are used in monitoring systems or systems with minimal resources.