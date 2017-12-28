# modern-compiler-implementation
This repository stores the code for the MiniJava compiler that is implemented as described by Modern Compiler Implementation in Java (2nd Edition)


This compiler goes through the following steps:

1. Lex - break the source file into individual words, or tokens

2. Parse - analyze the phrase structure of the program

3. Semantic Actions - build a piece of abstract syntax tree corresponding to each phrase

4. Semantic Analysis - determine what each phrase means, relate uses of variables to their definitions, check types of expressions, and request translation of each phrase

5. Frame Layout - place variables, function parameters,etc into activation records in a machine-dependent way

6. Translate - produce intermediate representation trees (IR trees), a notation that is not tied to any particular source language or target-machine architecture

7. Canonicalize - hoist side effects of expressions, and clean up conditional branches, for the convenience of the next phases

8. Instruction Selection - group the IR-tree nodes into clumps that correspond to the actions of the target-machine instructions

9. Control Flow Analysis - analyze the sequence of instructions into a control flow graph that shows all the possible flows of control the program might follow when it executes

10. Dataflow Analysis - gather information about the flowof information through variables of the program; (ie liveness analysis)

11. Register Allocation - choose a register to hold each of the variables and temporary values used by the program; variables not live at the same time can share the same register

12. Code Emission - replace the temporary names in each machine with machine registers