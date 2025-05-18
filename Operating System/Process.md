A process is a single active program in execution. It consists of the following components:
- **text section** - that includes the program's logic
- **Program counter** - that includes the current activity and next instruction address
- **Stack** - which hold temporary data such as function parameters, return addresses, local variables...
- **Data section** - which contains global variables
- **Heap** - contains dynamically allocated memory

A process has different states in its life cycle. It depends on the type of OS it is being executed on. There is:
- **two-state model** - which a process is either *running* during *dispatch* or not *running* during *pause*.
![[five-state-model.png]]
- **five-state model** - in which a process in in one of five states based on six transitions. They are:
	- **New** creates a process
	- **Ready** is waiting to be assigned to a processor.
	- **Running** means that instructions are dispatched to be executed.
	- **Waiting** is the process way of expecting an event, usually I/O completion
	- **Terminated** means the process has finished executing or has been aborted.

A process is implemented on an OS using a process control block(PCB) which contains:
- **Process state**; whether it's new, ready, running, waiting, terminated...
- **Program counter**, holds the address of the next instruction
- **CPU registers**; includes accumulator, [[Microcomputer and Interfacing|index registers]], stack pointers, [[Microcomputer and Interfacing|general-purpose registers]], condition code(holds the result of the latest operation)
- **CPU scheduling information** such as [[process priority]], [[start time]], [[arrival time]], [[burst time]],[[wait time]], event identity, scheduling queue pointers...
- **Memory-management information** such as [[page tables]], [[base register]], [[limit registers]]... 
- **Accounting information** such as process numbers, time limits, CPU usage...
- **I/O status information** such as I/O-process allocation, list of open files...
This allows processes to be saved when 