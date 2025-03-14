Three-address code is a generic form that can be implemented as **quadruples, triples, indirect triples, tree or directed acyclic graph(DAC)**. 
- **Quadruples** divides the instruction into *operator*, *argument-1, argument-2 and result* 
- **Triples** presents the instructions in three fields, i.e, *operator, argument-1 and argument-2*. However, this representation makes the code immovable while optimizing, since changing the order of instructions may cause errors.
- **Indirect triples** enhances the **triples** representation by using pointers rather than the actual values, thus not dealing with the code immovability problem.
Three address code is similar to a assembler code that it has:
- unary and binary operations
- copy statements
- unconditional and conditional jumps
- function calls using parameter specification
- indexed arguments
- address and pointer assignments
