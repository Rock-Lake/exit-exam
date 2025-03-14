Hierarchical analysis, also known as [[hierarchical analysis|syntax analysis]] or [[hierarchical analysis|parsing]] uses the tokens made by the [[linear analysis|lexical analyzer]] to create a tree structure called [[syntax tree]] to represent the grammatical structure of the token stream.
![[syntax analyzer.png]] 
where the interior node shows an operation and the leaf node represents the arguments of the operation. In this case, id 1,2,3, and 60 are the arguments.
The [[syntax tree]] is constructed by repeated usage of rules in [[context-free grammar]] and analyzed by [[Deterministic Push Down Automata]].
This syntax tree is then sent to the [[semantic analysis|semantic analyzer]].

When a parser detects a syntactic error, there are four general recovery strategies:
1. **Panic mode recovery**: delete input [[symbol]]s one by one until a valid token is found
2. **Phrase level recovery**: replace the local string with a valid token to continue parsing.
3. **Error productions**: 
4. **Global correction**: make few changes as possible 
