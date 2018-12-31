# simple-el-parser-test-suite
A simple Expresion Language parser

This test suite is created in the hope to allow other to implement the same behavior in what ever language they please.
If you've created an implementation of simple-el-parser, just let me know, we'll add a reference in this repository.

This test suite will serve as a reference point.

The construct allowed by this parser are intentionally reduced.
At the moment what is supported is the following:
- `abc` or `abc.def`: variable (value defined at runtime)
- `42`: integer/float litteral
- `3.14`: float literral
- `"Dudette"`: string litteral
- `&&`:  logical and
- `||`:  logical or
- `==`:  equality
- `!=`: inequality
- `>` : greater than
- `<`: lesser than
- `>=`: greater or equal
- `<=`: lesser or equal
- `(..)`: left and right parenthesis

Other operator will probably be added later.

Here are constructs used in js that won't be reproduced

- Function call
- control flow statement
- Rexep
- Bitwise operators
- comma
- void operator

Origin
----------

At first this project was created for magery (https://github.com/caolan/magery) a templating system which is language agnotic.
This module would work on expression parsing, and magery will do what ever is usefull to create a function/interpret it based on the results.

Why does it only produce an AST ?
--------------------------------------------------------------------------------

Since the produce will be used inside a templating system the way the compiled
expression is used is not up to the parser.

This part will be up to the templating system.
