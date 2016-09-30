# Lecture 2 (28/09/2016)

## Relation between grammars and regexps

The alternative operator used in regular expressions can be translated in grammar notation as:
`a | b` is the same as 
```
A -> a
A -> b
```
where A is a non terminal.

Repetition `a*` can be translated as follows:
```
A -> aA
A ->
```

The regexp form of defining productions/rules is a shorthand and is used in the BNF (Backus-Naur-Form) format for defining syntax.

## Ambiguous grammars

A grammar is called ambiguous if there is a word in the language that has more than one parse tree.
Ambiguity is different than non-determinism! For example
```
A -> a
A -> b
```

is perfectly fine; in fact it is just non-deterministic when trying to use derivations but there is no ambiguity.
There are various techniques to avoid ambiguity or to change an ambiguous grammar to a non-ambiguous one (more on this later).

## Definition of parser

A parser for a grammar is any program such that for any input string `w`:
- If the string w is in the language of the grammar, the parser finds a derivation of the string. In our case, it will always be a leftmost or a rightmost derivation.
- If the string w is NOT in the language of the grammar, the parser must reject it.
- The parser always terminates

## Lexical analysis (before parsing)

Before parsing there is a phase called lexical analysis (this will not be covered in the module, we assume we have the right input for a parser).
The lexer/scanner takes the source code and creates tokens of various types (e.g. keywords, numbers etc...).
There are various tools to generate lexer, for the UNIX world there is lex. The same applies to parsers; a good parser generator is yacc.

Lexical analysis works by transforming an initial regexp (for parser is a grammar) converting it into NFA then DFA (automata).

## Abstract machines

Abstract machines are useful in compiling programming languages because they provide an intermediate language for the compilation process.
Abstract machines are machines because they permit step-by-step execution of programs; they are abstract because they omit the many details of real (hardware) machines

Examples of abstract machines (see slides).
