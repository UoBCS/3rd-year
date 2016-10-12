# Lecture 5 (05/10/2016)

## LR vs LL

## Making LL machine deterministic using lookahead

We use one symbol of lookahead to guide the predict moves, to avoid predict moves that get the machine stuck soon after.
Formally this is done by "first and follow" construction which does not work for all grammars.

A grammar is not LL(1) if it is:

- Left recursive or
- Not left factored

To see if a grammar is LL(1) we must build the parse table for the predictive parser. If any element in the table contains more than one grammar rule right-hand side, then the grammar is not LL(1).

## FIRST sets

## FOLLOW sets
