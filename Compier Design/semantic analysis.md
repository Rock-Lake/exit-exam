The semantic analyzer uses the [[syntax tree]] and the information in the [[symbol table]] to check if the source program has semantic consistency and correct semantic meaning.

Another important part of semantic analysis is [[type checking]], i.e, checking that each operator(+, -, /, ...) has matching operands(int, char, float, ...) and saves the type information in either the [[syntax tree]] or [[symbol table]] for later use in [[intermediate representation|intermediate code generation]].

Some programming languages permit some type conversions called coercion.

After semantic analysis, the parse tree is sent to the [[intermediate representation|intermediate code generation]], however in cases where there are no compiler errors, the semantic analyzer translates the [[syntax tree|abstract syntax tree]] into [[abstract assembly tree]]; where it will be passed to the [[code optimizer]] and [[code generator]] phase.