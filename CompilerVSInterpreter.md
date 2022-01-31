| Basis of Comparison | Compiler | Interpreter |
|---------------------|-----------|--------------|
| Definition | A compiler is a program that translates a source program written in some high-level programming language (such as Java) into machine code for some computer architecture (such as the Intel Pentium architecture). | An interpreter reads an executable source program written in a high-level programming language as well as data for this program, and it runs the program against the data to produce some results. |
| Convert Source Code to Machine Code | Done in one go | Done line by line |
| Intermediate Code | Generated | will not be generated |
| Speed | Fast | Slow because it processes and interprets each statement in a program as many times as the number of the evaluations of this statement. For example, when a for-loop is interpreted, the statements inside the for-loop body will be analyzed and evaluated on every loop step  |
| Space Required | More | Less |
| Machine Independent/Dependent | Independent | Dependent |

### Similarity between both
Both interpreters and compilers (like any other program) are written in some high-level programming language (which may be different from the language they accept) and they are translated into machine code.

## Reference Link: 
[https://lambda.uta.edu/cse5317/notes/node3.html](https://lambda.uta.edu/cse5317/notes/node3.html)
