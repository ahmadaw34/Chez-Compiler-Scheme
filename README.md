this project is a Chez-Compiler that can compile a large subset of Scheme into Intel x86, 64-bit assembly language, and then, using the Newtide Assembler (nasm), assemble it into a standalone executable.

How to compile and run code in Scheme:
1) I set up a directory called testing and move the makefile into this directory, where all the chaos of temporary files can be contained without messing up the source files for the compiler.
2) run utop on linux terminal:
3) utop> #use "compiler.ml";;
4) utop> Code_Generation.compile_scheme_string "testing/goo.asm" "Scheme-Code";;
5) At this point, I have a file testing/goo.asm that I need to assemble. starting new terminal and the makefile does the rest, I type:
6) make goo
7) ./goo
8) make clean
