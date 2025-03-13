C++ is a [[compiler]]-based programming language, this means that any changes in the code requires the entire program to be translated into a machine-compatible executable program.

The structure of a C++ program can be easily explained using a simple example;
```
//My first C++ program
#include<iostream>

	void main(){
	std::cout<<"Hello World!";
}
```
This program, called **hello-world.cpp** prints a "Hello World!" message on a console. It has:
- **Comment**: specifically a single line [[comments|comment]] , the [[compiler]] ignores it since it is for the programmer to write notes on the program with affecting anything else.
- **Pre-processor:** it looks through the program for special keys before the [[compiler]]. This directs the [[compiler]] to include a copy of files specified in the angle brackets; in this case its the ***iostream***  file in the C++ standard library. 
- **Function:** any C++ program has a **main** function that is called automatically. This function has the type **void**, which means it will not return any value after the function finishes executing. The parenthesis is empty, thus having no arguments. More specifics can be explained in the [[functions]] section.
- **Statement:** the ```std::cout<<"Hello World!";``` statement has three parts: First, `std::cout`, which identifies the **st**andar**d** **c**haracter **out**put device (usually, this is the computer screen). Second, the insertion [[operator]] (`<<`), which indicates that what follows is inserted into `std::cout`. Finally, a sentence within quotes ("Hello world!"), is the content inserted into the standard output. Any C++ statement should end with a semi colon(;) to show the end of the statement.
The standard C++ library has different elements, such as **cout**, **cin**. In order to improve the readability of a program, we can declare the standard C++ library within a [[namespace]], the name space std.

```
//My second C++ program
#include<iostream>
using namespace std;
void main(){
	cout<<"Hello World!";
	cout<<"I'm a C++ Program";
}
```
