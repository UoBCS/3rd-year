# Lecture 3 (03/10/2016)

## Parsing and (non-)deterministic stack machines

If we can construct grammars for programming  languages, we should be able to use stack machines to
recognize correct programs and aid in their translation into assembly language.

One problem from translating a grammar to stack machine is nondeterminism. We can use backtracking but this
will make the computation time somewhere between n^2 and n^3 steps when recognizing strings of length n.

The parsing problem can be decomposed as follows:

- **What** the parser does: a stack machine possibly nondeterministic.
- **How** the parser knows which step to take, making the machine deterministic.

### Parsing stack machines

The state of the machine are of the form <sigma, w> where

- sigma is the stack, a string of symbols which may include non-terminals
- w is the remaining input

Definition: A context free grammar is an s-grammar iff every production's right hand side begins with a terminal symbol
and this terminal is different for any two productions with the same left-hand side.

We can fix that by using factoring:

Given a set of the form `A -> αβ1 | αβ2 | ... | αβn`

produce a new nonterminal Z and replace this set by:

```
A -> αZ
Z -> β1 | β2 | ... | βn
```

Now that we have a s-grammar for a production of the form `A -> aα` we just: read a, pop A, and push α onto the stack.

### LL and LR parsing

#### Terminology (see lecture notes)

#### Idea

Both use a parsing stack, but in different ways:

- LL: the stack contains a prediction of what the parser expects to see in the input
- LR: the stack contains a reduction of what the parser has already seen in the input

Theoretically LR is much more powerful than LL (however the latter is simpler).

## Further reading

http://www.cs.odu.edu/~toida/nerzic/390teched/cfl/Parsing/
