# Lecture 5 (05/10/2016)

## LL is top down

(See parse tree visualisation on lecture slides)

Top down parsers come in 2 forms: **backtracking parsers** and **predictive parsers**.

A predictive parser attempts to predict the next construction using one or more lookahead tokens (**recursive-descent parsing** and **LL parsing**).

## LL machine soundness proof

## LL exercise

Describe in general what the stuck states of the LL machine are, in which the machine can make no further steps, but cannot accept the input.
There are 3 cases, plus another one if the grammar is not good.

These are:

- When the stack is empty but we are left with characters in the input. This means that the machine cannot accept the input (i.e. the input is not in the language recognized by the grammar).
- When the LL parsing makes bad nondeterministic choices we cannot use match anymore.
- When a grammar is not a s-grammar (see definition in previous lecture).

## LR machine

Assume a fixed context free grammar. We can construct the LR machine for it.
The top of the stack is on the right.

Rules:

```
<ρ, aw> -> <ρa, w> // shift
<ρα, w> -> <ρA, w> // reduce for rule A -> α
```

```
<ε, w> is the initial state
<S, ε> is the final state
```
