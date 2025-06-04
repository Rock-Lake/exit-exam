A function is a collection of code that perform a specific task. The purpose of a function is modularity and re-usability; dividing a problem into smaller sub-problems, these sub-problems can be used in other programs when required.

There are two types of functions:
- **Builtin (Standard) functions:** functions which are predefined and ready to use in the standard C++ library.
- **User-defined functions:** functions which are designed and declared by the programmer.

Either way, all functions follow this syntax:
```
returnType functionName(parameterList){
	function body;
	return value;
}
```
Running a functions requires the function to be called as follows:
```
functionName(parameterList);
```

When running a function, there are two ways the parameter is inputted:
- **Passing By Value:** takes a copy of the parameter and runs the function, this won't modify the original data/variable.
- **Passing By Reference:** uses the value directly in the function, thus modifying the value. to do that we use a reference operator(&) with the variable to get the memory address of the variable.

Some functions require a default value as arguments(parameters), to do that, declare the value on the rightmost side of the parameter list.

The concept of functions comes with the concept of scopes. It essentially is how much of the data can be accessed from its place in the program. Functions create their own **local scope**, where variables with the same name as ones defined outside the function can run without error. Data defined outside any function but inside the program is under **global scope**, that means all functions can be accessed by the entire program. However, variables in local scope are given attention before global variables. ^c98713

Functions can have the same name, if the arguments number/type changes between different functions. This property of functions called **overloading** allows for customization of the same function for more specific application.  ^1ec80e

Functions that require repeating the same actions repeatedly in a spiral manner, can call themselves; these are called recursive functions.
```
returnType functionName(parameterList){
	functionName(parameterList);
	return value;
}
```