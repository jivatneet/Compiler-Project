# Compiler-Project
This repository contains the code for a COMPILER designed for the course CS F363-Compiler Construction in BITS Pilani.

## modules
The project has been implemented in a pipelined manner with the modules consisting of:
1. Lexer (lexer.c)
2. Parser (parser.c)
3. AST creation (ast.c)
4. Symbol Table construction, Type extraction and Scoping (symbol.c)
5. Semantic Analysis and Type checking (semanticAnalyzer.c)
6. Intermediate Code Generation (intermediateCode.c)
7. Code Generation in Assembly (codeGen.c)

## compatibility
- gcc version 5.0 or above
- NASM 2.14.02 (64-bit compatible)

## usage
1. Use `make` to compile the C-code into executable binary `compiler`
2. For running the executable for testcase.txt (testcases provided for Stage 1, Semantic analysis and Code generation) and     generating the assembly file code.asm
 `./compiler testcase.txt code.asm`
3. Select the appropriate option (0-9) from the driver menu to test the desired modules of the compiler
4. For producing the binary from .asm file
(**NOTE** : code.asm is generated only if testcase.txt has no semantic errors. For viewing the errors in the code, use option '8' of the driver menu)

  - Ubuntu 16.04
  ```
  nasm -f elf64 -o output.o code.asm
  gcc output.o
  ./a.out
  ```
  
  - Ubuntu 18.04 and higher versions
  ```
  nasm -f elf64 -o output.o code.asm
  gcc output.o -no-pie
  ./a.out
  ```
