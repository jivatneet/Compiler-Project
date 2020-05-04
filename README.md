---------ERPLAG COMPILER----

1.Pre-requisites
Ubuntu 16.04
GCC version 5.4.0 
NASM 2.14.02 (64-bit)

2.Instructions for running testcases

i. Use make to compile the compiler C-code

make
./compiler testcase.txt code.asm

ii. Compile and run asm file using NASM

a. Ubuntu 16.04

nasm -f elf64 -o output.o code.asm
gcc output.o
./a.out

b. Ubuntu 18.04 and higher versions

nasm -f elf64 -o output.o code.asm
gcc output.o -no-pie
./a.out

