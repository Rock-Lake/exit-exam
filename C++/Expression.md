An expression is a statement that computes and returns a value. It is made up or **operators, operands** in the form of [[Constants|constants]] or [[Variables|variables]].

Operator is a language specific [[hierarchical analysis|syntactical token]] that requires an action to be taken. For any given operator there will at least be one operand.

In C++ syntax, there are 7 basic types of operators:
1. **Arithmetic Operator:** used in basic math they are addition(+), subtraction(-), multiplication(\*), division(/), and remainder(%). ^e1dedc
2. **Relational Operator:** compares two values and outputs a [[Variables#^c07ee8|boolean]] result. They are equality(\==), inequality(!=), less than(<), greater than(>), less than or equal to(<=), and greater than or equal to(>=).
3. **Logical Operator:** computes logical expressions and outputs a [[Variables#^c07ee8|boolean]] result. They are logical NOT(!), AND(&&) and OR(||).
4. **Increment and Decrement Operators:** adds(++) and subtracts(--) a numerical value by 1. They can be added in prefix or postfix form and can affect the final result.
5. **Assignment Operator:** written as (=), it takes the value on the right side-usually a constant-and applies it to the variable on the left side. It can be combined with an [[Expression#^e1dedc|arithmetic operator]] to write a shorthand expression of `x = x operator y` as `x operator= y` ^1b496d
6. **Conditional Operator:** similar to a [[Conditional|conditional]], it returns a value based on a given condition. it is written as `x = (y relational_operator z ? y:z)`.
7. **Sizeof() Operator:** it calculates the size of any data in its parenthesis in bytes.

**NB**
- To get a floating point number from diving 2 [[Variables#^c07ee8|integrals]], you must [[#^2439e5|type cast]] one of the integers into a floating point.
- The remainder operator expects both of its operands to be [[Variables#^c07ee8|integrals]]
- It is illegal to divide by zero; there's a slight chance you will blow the machine up
- It is possible to compare char and the memory addresses of [[strings]]
- adding increment/decrement operator in prefix form changes the variable before the outcome is used in the expression while postfix form affects the variable after the expression is valued.

When combining multiple operators in one expression, there's a precedence of operators that is followed unless a parenthesis is used to indicate order. 

| Operator type | subtype        | Operator              |
| ------------- | -------------- | --------------------- |
| Unary         |                | !,++,--, -            |
| Arithmetic    | Multiplicative | \*, /, %              |
|               | Additive       | +,-                   |
| Relational    | Inequality     | <,>,<=,>=             |
|               | Equality       | \==, !=               |
| Logical       | AND            | &&                    |
|               | OR             | \|\|                  |
| Conditional   |                | ?:                    |
| Assignment    |                | =, +=,-=, \*=, /= ,%= |
If the operators are in the same precedence, then the operation is performed right-to-left.

When evaluating an [[#^e1dedc|arithmetic expression]] of values with different data types, the program implicitly converts one datatype to another for easier execution; this is called *implicit type coercion*. To avoid implicit type conversion, C++ provides explicit type conversion through a cast operator. The cast operator, also known as type casting can be written as `static_cast<dataTypeName(expression)` ^2439e5

In addition to basic operators, some C++ libraries [[overload]] symbols to perform special actions. The most used are `<<`, referred to as *stream insertion operator* and `>>` known as *stream extraction operator* ^b761c5