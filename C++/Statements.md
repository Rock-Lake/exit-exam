A statement is a computational step of a program when executed; produces a change in the program's state. In C++, statements control the order of the program's execution, also known as **flow control**.

C++ provides different forms of statements:
## **Simple Statement**
it is a computation that ends with a semicolon. It can be a declaration, an expression or a null statement as long as it ends with a semicolon. An example of a simple statement is a *input statement* where the computer is getting data from the keyboard. ^e3f3b6
## **Compound Statement** 
It is a unit of code consisting of a one or more simple statements, usually a declaration, definition and other statement enclosed in a brace. This allows to put multiple statements in one space or introduce a new [[scope]].
```
statement
{
	statement;
	statement;
	statement
	{
		statement;
	}
}
```

## **Selection Statement** 
Also known as *conditional statement*, it is used for specifying alternate paths of execution depending the the outcome of a logical condition. Depending on the number of alternative paths, C++ provides 3 branches of conditional syntax: ^d2fe3e
- **One-way selection**: this selection executes the statement inside only if the expression is true. Its general form is:
		```
		if (expression)
		{
			statement;
		}
		``` 
- **Two-way selection** the result of the expression is true then, the statement in *if* is executed, otherwise the statement in *else* is executed. Its general form is as follows:
		```
		if (expression)
		{
			statement;
			statement;
		}
		else
		{
			statement;
		}
		```
- **Multiple-way selection:** this selection can be implemented in one of two ways, using a compound statement of nested if-else statements or a *switch* statement.
	- **Nested If:** if the expression is true then the statement in *if* is executed, otherwise the *if* statement nested in the *else* section is checked.
			```
			if (expression)
			{
				statement;
			}
			else if (expression)
			{
				statement;
			}
			else
			{
				statement;
			}
			```
	- **Switch:** provides a way of choosing between a set of choices based on the value of an expression.
			```
			switch (expression)
			{
				case value1:
					statement_1;
					break;
				case value2:
					statement_2;
					break;
				.
				.
				.
				case valuen:
					statement_n;
					break;
				default:
					statement;
			}
			```
	**NB:** When writing the expression for the conditional, the computer will predict the expression's outcome and return the expression result faster. This is called *short-circuit evaluation*.
## **Iterative Statements**
Also known as *loops*, these statements repeat a series of instruction a number of times, depending on the condition it was given. In C++ loops can be arranged in one of three ways: ^4d5182
- **for loop:** This is the simplest iterative statement that follows the general look:
		```/* 
		Expression 1 is usually a a variable declaration and/or value assignment int x = 0;
		Expression 2 expression the maximum range of the loop; x <= limit
		Expression 3 is the number of steps the loop increases/decreases the value like x++
		*/
		for (expression_1;expression_2; expression_3)
		{
			statement;
		}
		```
- **while loop:** this iterative statement will repeat the inner statement while the expression is true.
		```
		while(expression)
		{
			statements;
		}
		```
- **do-while loop:** even though it is similar to the *while* loop, it executes the statement then checks for the expression's condition.
		```
		do{
			statement;
		}
		while(expression);
		```
## Jump Statements
These statements alter the flow of statements by either starting, stopping or skipping some sections ([[scope]]) of code. There are 4 types of jump statements: ^3c2bc1
- **Break statement:** this statement causes an exit from [[#^4d5182|loops]] or [[#^3c2bc1|selections]], thus moving the [[scope]] of the program from the inner block to the outer. If `break` is used outside a loop or a selection, it will cause an error. ^44fdde
- **Continue statement:** this statement causes the loop to end and start the next iteration. Just like [[#^44fdde|break]] statement, the `continue` statement can only work inside a [[#^4d5182|loop]]. 
- **Go-To statement:** this statement causes the program to jump to the part of the program labeled in the go to statement. For example:
```
bool test = true;

if(test)
	goto label_1;
else
	goto label_2;

label_1:
	cout<< "label 1";
label_2:
	cout<< "label 2";
```
will jump to the program under label 2 if test is false.
- **Return statement:** this statement returns the result of a [[functions|function]] to its caller.