| Basis of Comparison | Compiler | Interpreter |
|---------------------|-----------|--------------|
| Definition | A compiler is a program that translates a source program written in some high-level programming language (such as Java) into machine code for some computer architecture (such as the Intel Pentium architecture). |
| Convert Source Code to Machine Code | Done in one go | Done line by line |
| Intermediate Code | Generated | will not be generated |
| Speed | Fast | Slow because it processes and interprets each statement in a program as many times as the number of the evaluations of this statement. For example, when a for-loop is interpreted, the statements inside the for-loop body will be analyzed and evaluated on every loop step  |
| Space Required | More | Less |
| Machine InDependent/Dependent | Independent | Dependent |