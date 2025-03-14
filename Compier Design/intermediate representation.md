In the process of translating a source program into target code, a compiler constructs one or more intermediate representations, which can be in many forms; such as [[syntax tree]].
For a translation to be called an intermediate representation, it should be easy to produce and and translatable into the target machine.
The type of intermediate code used depends on the application:
- [[three address code]]s, such as Quadruples, triples, indirect triples and abstract syntax trees are used for machine-independent optimizations and machine code generation
- Static Single Assignment form(SSA) for more effective optimizations
- Program Dependence Graph(PDG) for auto-parallelization, instruction scheduling and pipelining.
