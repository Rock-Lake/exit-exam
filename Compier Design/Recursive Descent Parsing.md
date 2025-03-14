It is a method of parsing where it uses [[context-free grammar]] to recursively parse the input symbols until the terminals are located.

This is its algorithm:
1. Create a root node that has Starting symbol (S)
2. Use two pointers that point to the tree and left most input symbol
3. Expand the tree using the S-production rule
4. move the tree pointer to the leftmost symbol of the sub tree
5. If the terminal symbol (a,b,c,...) on the tree pointer is the same as the input pointer, move both pointers to the right.
6. If the terminal symbol on the tree pointer isn't the same as the input pointer, backtrack to a non-terminal and use an alternative production rule and go to step 3.
7. if the input pointer reached the end of the input string($), the parser has finished.
