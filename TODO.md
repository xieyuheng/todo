# hindley-milner.js

persons/luis-damas/1985-type-assignment-in-programming-languages
persons/joseph-e-stoy/1977-denotational-semantics--the-scott-strachey-approach-to-programming-language-theory
persons/john-alan-robinson/1965-a-machine-oriented-logic-based-on-the-resolution-principle

# x-lisp.js

persons/luca-cardelli/1993-subtyping-recursive-types
finish xieyuheng/x-lisp.js -- recursive structural type
- use the idea of combinators -- by putting env and ctx to the last currying argument position.
- use the idea of propagator model to implement type system.
cicada-lang/lambda -- equal of recursive defined function mod partial evaluation

## combinatory-logic

> combinatory logic and dependent type theory

using combinatory logic as the domain of language with dependent type:
- a type (set) is a predicate-like element
- only need one judgement `|-`
- all bound variable can be compiled out: lambda, pi, sigma
- infinite sum and product can be handled by high order functions:
  - first argument is a type, second argument is a function

persons/j-roger-hindley/1997-basic-simple-type-theory
persons/j-roger-hindley/2008-lambda-calculus-and-combinators--an-introduction
persons/haskell-curry/1951-outlines-of-a-formalist-philosophy-of-mathematics
persons/haskell-curry/1963-foundations-of-mathematical-logic
persons/haskell-curry/1956-combinatory-logic--volume-1
persons/haskell-curry/1970-combinatory-logic--volume-2

> dependent type and combinatory logic

maybe dependent type is more easy to develop in combinatory logic.

> the S of combinatory logic is much like the dup of interaction nets

## recursion theory

study recursion theory -- to understand kleene's mu operator

- https://en.wikipedia.org/wiki/mu_operator
- https://en.wikipedia.org/wiki/Computability_theory
- https://plato.stanford.edu/entries/recursive-functions/

## algebraic-subtyping

topics/type-theory/2016-algebraic-subtyping--tephen-dolan.pdf

# inet and propagator

persons/robin-milner/2009-the-space-and-motion-of-communicating-agents

# cicada

persons/robin-milner/1979-edinburgh-lcf--a-mechanised-logic-of-computation
persons/peirce/1880-on-the-algebra-of-logic -- early denotational semantics for logic

## kan complex

2011-simplicial-structures-in-topology--davide-l-ferrario--renzo-a-piccinini.pdf
2023-an-elementary-illustrated-introduction-to-simplicial-sets--greg-friedman.pdf
2023-higher-categories-and-homotopical-algebra--denis-charles-cisinski.pdf
