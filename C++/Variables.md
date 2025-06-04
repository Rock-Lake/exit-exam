Variables are portion of a computer's memory set aside to store a value. It requires an **identifier** and a **datatype** to create a unique variable.

The identifier of a variable has a few rules:
- It can't start with a number or a symbol except underscore(\_) 
- it can't use spaces, punctuation marks or symbols except underscore(\_)  as identifiers on its own or within other identifiers
- it can't be the following since they are C++ keywords:
```
 alignas, alignof, and, and_eq, asm, auto, bitand, bitor, bool, break, case, catch, char, char16_t, char32_t, class, compl, const, constexpr, const_cast, continue, decltype, default, delete, do, double, dynamic_cast, else, enum, explicit, export, extern, false, float, for, friend, goto, if, inline, int, long, mutable, namespace, new, noexcept, not, not_eq, nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, return, short, signed, sizeof, static, static_assert, static_cast, struct, switch, template, this, thread_local, throw, true, try, typedef, typeid, typename, union, unsigned, using, virtual, void, volatile, wchar_t, while, xor, xor_eq 
 ```
 C++ variables are **case sensitive**, that means identifiers written in capital letters is not the same as written in small letters.

The datatype of a variable is a set of values that can be manipulated with a set of allowed operations. ^c136b3

In C++, there are 3 categories of datatypes:
- Simple data type: ^c07ee8
	- integrals such as int, short,long, char, bool
	- floating points such as float, double
	- enumerations, a user-defined datatype
- Structured data type such as string, array,
- Pointers
**NB:** integral datatypes such as char, int, long and short have a range of positive and negative numbers. By using **unsigned** before the datatype, you can change the range to start from 0.
The size of the portion of memory set aside for the variable depends on the datatype of the variable.

Before a variable can be used in a program, it must first be declared. In C++, the syntax rule to declare a variable is ```dataType identifier;```. We can also assign a value to the variable using the [[Expression#^1b496d|assignment operator]] like this:
```C++
dataType identifier = expression;
//or
dataType identifier;
variable = expression;
```

Some data must stay the same throughout the program. In C++, you can use a **named constant** to instruct the program to mark memory locations in which data is stored unchanged throughout the program's execution. The syntax to declare a named constant is `const dataType IDENTIFIER = value;`^098fda

**NB:** when defining a constant floating-point number, the value must be written with 'f' at the end. For example; `const float PI = 3.1415f`