Linear analysis, also known as '[[linear analysis|Lexical analysis]]' or '[[linear analysis|scanning]]' reads the stream of characters that makes up the source code left-to-right and groups the characters into meaningful sequences called [[lexemes]]. Each [[lexemes|lexeme]] is outputted from the lexical analyzer as a token in the form *(token-name, attribute-value)* where:
- *token-name* is an abstract symbol used in [[hierarchical analysis|syntax analysis]]  
- *attribute-value* points an entry in the [[symbol table]]  
and forwarded to [[hierarchical analysis|syntax analysis]].

Other than identifying [[lexemes]], lexical analyzers perform the following:
- strip out comments and whitespace,
- correlate compiler error messages
- expand macros
When designing lexical analyzers, the approach of implementation can affect efficiency and ease of implementation. As a principle; the closer the implementation is to machine language the more efficient but hard to implement.
Lexical analyzers uses two pointers to separate tokens from input strings; the **Begin pointer** and the **Look Ahead pointer**. Both point to the starting character, and the **Look Ahead pointer** goes through the input string until it finds a different lexeme where both pointers jump to the next character and the located lexeme is converted into a token.
When lexical analyzer read the stream of characters from secondary memory, using an input buffer to store the input strings before scanning can improve efficiency.
The input buffer can be overwritten if the block of data is larger than the first buffer. To solve this, we can use a two-buffer scheme, where both buffers have a sentinel/end-of-buffer(eof) at the last space to connect the two buffers.
In this way, if the first buffer is filled the pointers move to the second buffer while the first buffer is overwritten.
Like all things, lexical analyzer have errors, they are:
- lexemes that exceeded character limit (bound)
- illegal character, ex: int $abc is an illegal character
- unterminated strings or comments
when detecting the above errors, lexical analyzer have different recovery methods:
- **Panic mode recovery**: delete successive characters of the remaining input until it forms a valid token
- insert a missing character to the remaining input, ex: fo -> for
- replacing an incorrect character, ex: fir -> for
- transpose adjacent characters, ex: fi -> if
