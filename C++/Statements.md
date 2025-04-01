A statement is a computational step of a program when executed; produces a change in the program's state. In C++, statements control the order of the program's execution, also known as **flow control**.

C++ provides different forms of statements:
- **Simple Statement:** it is a computation that ends with a semicolon. It can be a declaration, an expression or a null statement as long as it ends with a semicolon. An example of a simple statement is a *input statement* where the computer is getting data from the keyboard. ^e3f3b6
- **Compound Statement:** is a unit of code consisting of a one or more simple statements, usually a declaration, definition and other statement enclosed in a brace. This allows to put multiple statements in one space or introduce a new [[scope]].
- **Selection Statement:** also known as *conditional statement*, it is used for specifying alternate paths of execution depending the the outcome of a logical condition. Depending on the number of alternative paths, C++ provides 3 branches of conditional syntax: ^d2fe3e
	- **One-way selection**: this selection executes the statement inside only if the expression is true. Its general form is:
		```
		if(expression)
		{
			statement;
		}
		``` 
	- **Two-way selection** the result of the expression is true then, the statement in *if* is executed, otherwise the statement in *else* is executed. Its general form is as follows:
		```
		if(expression)
		{
			statement;
			statement;
		}
		else
		{
			statement;
		}
		```
	- **Multiple-way selection:** 