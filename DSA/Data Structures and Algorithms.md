This course focuses on teaching the foundations of writing clean and efficient code using well-understood and tested techniques.

# Introduction
The measure of a program's performance is usually time and space(memory) usage. The time usage, also defined as execution speed; is the amount of time it takes the program to compute instructions. Ignoring hardware restrictions, some programs can perform faster even running on the same hardware and working the same problem. This is usually depend on how the program organizes the data required to solve the problem and the sequence of steps it took to solve the problem.
# Data Structures
Any form of information processing or communication requires data to be stored and accessed when needed. A general abstract of a data storage is that of a **Container Abstract Data Type**. A container describes data structures that store and give access to objects. A container can be created, copied, destroyed, emptied of its objects, queried of the number of objects in it, ask its capacity, merge or intersect with another container. ^035aa0

Many data structures are used(operated) in 5 basic ways:
- **Read** - look at each object in the data structure ^70d2a5
- **Search** - check for a object within the data structure ^e63471
- **Insert** - Add a new object to the data structure ^8c0303
- **Update** - modify a object in the data structure ^d879d9
- **Delete** - remove a object from the data structure ^2d8491

Containers can be split into general classifications:
- **Simple containers** - which store individual objects
- **Associative Containers** - which store keys and their records. For example; [[Database Systems|databases]] 
We will focus on simple containers and their data structures.

There are many data structures used to efficiently store, access and modify data; each with their own strengths and weaknesses. Choosing a data structure, not only change how the program interacts with the data, but also drastically affect the program's performance.

There are different data structure depending on the memory allocation. They are:
- Contiguous allocation such as [[Array|Arrays]], [[List|Lists]], [[Stack|Stacks]], [[Queue|Queues]] 
- Linked allocation such as [[Linked List|Linked Lists]], [[Tree|Trees]], [[Graph|Graphs]], [[Deque|Deques]] 
- Indexed allocation such as [[Vector|Vectors]], [[Inode|Inodes]] 
# Algorithm Analysis
An algorithm is a set of instructions for completing a specific task. The goal of algorithm analysis is to take a block and determine its efficiency. However we can't label algorithms on the number of steps, since the number of steps an algorithm takes can't be a single number due to the changing size of data the algorithms has to compute. ^854a22

The best way to compute an algorithm's efficiency is to determine its asymptotic runtime or asymptotic memory. Asymptotic runtime is a function that determines the expected number of steps to ever increasing data size to compute. Described as Big O notation, it describes the worst case of an algorithm execution unless specified otherwise. 

For example, given this code:
```C++
	for ( int i = 0; i < capacity_old; ++i ) {
		array[i] = array_old[i];
	}
```
the Big O notation of this loop is $\Theta(n)$ since the code in the inner scope will be repeated *n* times if the range of the for loop increases *n* amount.

There are different Big O notations of different algorithms; but most fall under the following:
- $\Theta(1)$, also called constant time, these algorithms will not be affected by size of the data it computes
- $\Theta(N)$, also called linear time, these algorithms scale linearly with data size
- $\Theta(N^2)$, also called exponential time, these algorithms scale exponentially with data size.
- $\Theta(log_{2}N)$ or $\Theta(logN)$ known as logarithmic time, these algorithms scale logarithmically with data size.

When calculating Big O notation of an algorithm, we remove all constants in the expression, since constants don't change the general efficiency of the algorithm.
For example:
- O(N/2) will be O(N)
- O($N^2 + 10$) would be expressed as $O(N^2)$
- O(100N) would expressed as O(N)

To fully visualize the impact of asymptotic runtime on the efficiency of programs, we can see some popular algorithms:
- Sorting
	- [[Bubble Sort]]
	- [[Selection Sort]]
	- [[Insertion Sort]]