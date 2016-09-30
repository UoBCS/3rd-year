# Lecture 1 (26/09/2016)

## Admin stuff

Reading:
- Standard book (though not followed linearly by Hayo): "Compilers: Principles, Techniques and Tools"
- The lectures will be mostly guided by research (especially on compiling functional langauges)

Syllabus:
- LL and LR parsing using stack machines
- Compiling C-like languages: stack frames, x86
- Compiling functional language

Pre-requisites:
- Grammars and automata
- Computer architecture and C/C++
- Functional programming

## What is a compiler

A compiler consists of a sequence of transformations between programming languages (from source text to binaries/bytecode).
These transformations must preserve the semantics (meaning) of the program.

We can represent these states in as abstract machine states (see LLVM/clang and its IR or Intermediate Representation).

In this module we will cover:
- LL and LR (parsing) that transforms a grammar into stack machines (opposite to register machines)
- Stack frames for function calls (recall C/C++ in 2nd year) that transform variables/names into indices that'll
be used as addresses
- SECD/CEK machine with closures for functional programs. function -> code + environment.

All the above output is directly understandable by the machine.

## Parsing

Parsing deals with the syntax of the code. It is one of the first steps in the compilation process (after lexical
analysis).
It turns a source file into a tree data structure (parse tree). The remaining phases of the compiler will
manipulate (tree walking/syntax-directed translation/compositional semantics) this data structure.

It's easy to manually build a parser and it's even easier to use parser generator.

(look at Dyck language example - in the slindes).

## Grammars

There are various types of grammars (context-sensitive, context-free etc...) but only context-free are useful
for representing programming languages.

A context-free grammar consists of
- *terminal* symbols
- *non-terminal* symbols
- among the non-terminals there is a *start symbol* S
- *rules/productions* of the form: A -> X_1 ... X_n where n >= 0, A is non-terminal and X_i are symbols.

### Convention

- Greek letters are used for strings of symbols that may contain both terminal and non-terminals
- A, B, ... are for non-terminals
- S is the starting symbol
- a, b, ... are for terminals
- v , w , x, y , z are used for strings of terminal symbols
- X , Y , Z are used for grammar symbols that may be terminal or non-terminal

### Equivalence of parse trees and derivations