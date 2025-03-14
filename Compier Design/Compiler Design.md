### What is a compiler?
- An executable program that translates a source code, usually written in a high level language, into an equivalent target code, which often is either machine code or intermediate code. During translation, any detected errors in the source program will be notified to the user.
### What are the different classification of compilers?
- Compilers can be classified into [[single-pass]], [[multi-pass]], [[load-and-go]], [[debugging/optimizing]] depending on the method of construction or its functionality.
### What are the main parts of compilation?
- There are two parts to compilation; [[Analysis]] and [[Synthesis]]. The analysis part breaks down the code into its fundamental parts and creates an [[intermediate representation]] of the source program, while the synthesis part builds the target code based on the [[intermediate representation]].
- This form of separation between the  [[Analysis|analysis]] and [[Synthesis|synthesis]] with the [[intermediate representation|intermediate code]] bridging the two is beneficial when compilers translate a single source language into many target languages.