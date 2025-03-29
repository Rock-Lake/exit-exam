The C++ syntax has a few different ways to write comments on a C++ program. It can be:
- ```//``` - A single line comment. You can write it separately or with a statement as long as it is the last thing on that line. For example:
	- ```std::cout<<"Hello World!"; //This prints Hello world``` is valid, however
	- ```std::cout<<//This prints hello world "Hello World!;``` makes the [[Compiler Design|compiler]]  think that ```"Hello World";``` is part of the comment.
- ```/* */``` - A block comment. This makes any written text between ```/*``` and ```*/```  will be ignored by the compiler, including multiple lines.