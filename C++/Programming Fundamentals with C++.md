# Introduction

Problems that occur day-to-day can be solved by computers in various ways. However, all computer solutions require to go through a formal problem solving method. They are:
- **Defining the Problem:** We must understand the specifics of the problem. Its root cause and the behavior of the expected solution; the required data and the procedures needed to achieve the result are necessary to create a picture of the problem.
- **Planning the Solution:** dividing the problem into a number of smaller sub-problem to be solved with a precise method; a set of well defined steps called an [[algorithm]]. This results in a series of steps written in normal language and some mathematical notations called a **pseudo-code**.
- **Coding the Program:** Since we can't copy the pseudo-code into the computer and expect it work, we have to translate it into a [[programming language]]. There are various programming languages with different [[syntax rules]].
- **Testing the Program:** Most programs can't run perfectly the first time; they can produce errors based on the programmer's fault or in its logic. These errors are detected during testing the program, and appropriate revision must be made. This process of repeatedly coding and testing is called **implementation**.
- **Documentation:** Humans, unlike computers, can't remember every little detail about their experiences, thus compiling related documents throughout the program development is essential. The documentation should include:
	- Problem Definition
	- Explaining the steps of the algorithm
	- The problems encountered during the coding and testing of the program
	- Explanation of important or ambiguous parts of the program, usually through [[Comments|comments]] on the code.
	- a written copy of the program
	- a user manual of the program's usage
Now that we have a basic understanding of solving a problem through a program, let us see its implementation through C++.

# C++
C++ is a [[Compiler Design|compiler]]-based programming language, this means that any changes in the code requires the entire program to be translated into a machine-compatible executable program.

The structure of a C++ program can be easily explained using a simple example;
```C++
//My first C++ program
#include<iostream>

int main()
{
	std::cout<<"Hello World!";
	return 0;
}
```
This program, called **hello-world.cpp** prints a "Hello World!" message on a console. It has:
- **Comment**: specifically a single line [[Comments|comment]] , the [[Compiler Design|compiler]] ignores it since it is for the programmer to write notes on the program with affecting anything else.
- **Pre-processor:** it looks through the program for special keys called *pre-processor directives* before the [[Compiler Design|compiler]]. This directs the [[Compiler Design|compiler]]  to include a copy of files specified in the angle brackets; in this case its the ***iostream***  file in the C++ standard library. 
- **Function:** any C++ program has a **main** function that is called automatically. This function has the type **int**, which means it will return a zero after the function finishes executing. The parenthesis is empty, thus having no arguments. More specifics can be explained in the [[functions]] section.
- **Statement:** the ```std::cout<<"Hello World!";``` statement has three parts: First, `std::cout`, which identifies the **st**andar**d** **c**haracter **out**put device (usually, this is the computer screen). Second, the [[Expression#^b761c5|insertion operator]] (`<<`), which indicates that what follows is inserted into `std::cout`. Finally, a sentence within quotes ("Hello world!"), is the content inserted into the standard output. Any C++ statement should end with a semi colon(;) to show the end of the statement.
The standard C++ library has different elements, such as **cout**, **cin**. In order to improve the readability of a program, we can declare the standard C++ library within a [[namespace]], the name space std.

```C++
//My second C++ program
#include<iostream>
using namespace std;
int main()
{
	cout<<"Hello World!";
	cout<<"I'm a C++ Program";
	return 0;
}
```

This program is nice and all, but it does not do anything other than printing [[Strings|strings]]. Let's improve that by introducing [[Variables|variables]].

```C++
#include<iostream>
using namespace std;
int main()
{
	/*Variable declarations. A statement such as double length; instructs the system to allocate memory space and name it length.*/
	double length;
	double width;
	double area;
	double perimeter;
	double length;
	cout << "Program to compute and output the perimeter and "
		 << "area of a rectangle." << endl;
	length = 6.0;
	//Assignment statement. This statement instructs the system to store 6.0 in the memory space length.
	width = 4.0;
	return 0;
}
```
In this program called **area\_perimeter.cpp**, it stores 2 values of *length* and *width* and will compute the perimeter and area of a rectangle. To do that we need an [[Expression|arithmetic expression]].

```C++
#include <iostream>
using namespace std;
int main()
{
	double length;
	double width;
	double area;
	double perimeter;
	double length;
	//Variable declarations. A statement such as instructs the system to allocate memory
	space and name it length.
	cout << "Program to compute and output the perimeter and " << "area of a rectangle." << endl;
	length = 6.0;//Assignment statement. This statement instructs the system to store 6.0 in the memory space length.
	width = 4.0;
	perimeter = 2 * (length + width);
	area = length * width;//Assignment statement. This statement instructs the system to evaluate the expression length * width and store the result in the memory space area.
	cout << "Length = " << length << endl;
	cout << "Width = " << width << endl;
	cout << "Perimeter = " << perimeter << endl;
	cout << "Area = " << area << endl;
	//Output statements. An output statement instructs the system to display results.
	return 0;
}

```
This program computes the area and a perimeter of a rectangle with 6 units of length and 4 units of length. To compute a rectangle of a different length, a programmer must change the value of length and width of the program. This doesn't account for the average user who doesn't know C++ syntax. To change this, we require an [[Statements|input statement]].