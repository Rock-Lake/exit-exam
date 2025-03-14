Analysis, also known as the [[Analysis|front-end]] is the part of the compiler that breaks up the source code into smaller pieces and imposes a grammatical structure that makes up the [[intermediate representation]] of the source program.
If the source program has either a syntax or semantic error that the analysis part can detect, it will send an informative error message to the user.
It also collects information about the source program and stores it in a [[symbol table]].
Most, if not all software tools that manipulate the source program first perform some kind of analysis. Some examples include:
- [[Structure Editors]]
- [[Pretty Printers]]
- [[Static Checkers]]
- [[Interpreters]]
During compiling, analysis consists of three phases; [[linear analysis]], [[hierarchical analysis]], and [[semantic analysis]]. 
After analysis, the [[intermediate representation]] and the [[symbol table]] is passed to the [[Synthesis]] part of the compiler.