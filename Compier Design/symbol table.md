Symbol table is a data structure that store information about the occurrence of various entities such as variables, functions, objects, classes, interfaces...
Depending on the language used, a symbol table can be used to:
- store the names of all entities at one place.
- verify if a variable has been declared
- implement [[type checking]] 
- find out the scope of a name(scope resolution)
Symbol tables are implemented as lists, binary search trees, hash tables depending on the amount of data that the compiles has to handle. These data structures are used because they have the following methods/functions:
- insert() - used frequently during [[Analysis|analysis]];it stores the value, state, scope and type about the [[symbol]]. 
- lookup() - checks the symbol exists in the symbol table. This can vary across programming languages but it either returns 0 if it didn't exist or returns the symbol's stored attribute.
Compilers maintain two types of symbol tables to differentiate scopes in the program. They are:
- **Global symbol table**: that can be accessed by all procedures
- **Scope symbol table**: that are created for each scope in the program.
These two tables are related in a hierarchical structure and their relation is stored in the [[semantic analysis|semantic analyzer]]; and whenever a name is searched in a symbol table, the symbol tables are searched from specific-to-general.