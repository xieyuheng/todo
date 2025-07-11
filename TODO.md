# lattice theory

persons/george-grätzer/1978-general-lattice-theory.md

# x-lisp.js

type system as lattice
univalent analysis of relation -- wikiepdia page of HM
computational analysis of formal system

persons/luca-cardelli/1993-subtyping-recursive-types

xieyuheng/x-lisp.js -- recursive structural type

- use x-lisp as the denotational semantics of x-lisp, specially for type system
  - maybe use explicit substitution for runtime semantics

- equal of recursive defined function mod partial evaluation
- use the idea of combinators -- by putting env and ctx to the last currying argument position.
- use the idea of propagator model to implement type system.
- implement not as type operator, which is needed to view pattern in pattern matching as type.

## random

2008-the-seven-virtues-of-simple-type-theory.pdf

## theorem prover

robin-milner/1979-mathematical-foundations-of-computer-science---proceedings
robin-milner/1984-the-use-of-machines-to-assist-in-rigorous-proof

robin-milner/1972-logic-for-computable-functions-description-of-a-machine-implementation
robin-milner/1976-models-of-lcf
robin-milner/1978-a-metalanguage-for-interactive-proof-in-lcf
robin-milner/1979-edinburgh-lcf--a-mechanised-logic-of-computation

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

## foundation of mathematics

learn from hilbert

- my understanding of the logic of mathematics is shaped by type theory now,
  maybe i should learn the other way.

## recursion theory

study recursion theory -- to understand kleene's mu operator

- https://en.wikipedia.org/wiki/mu_operator
- https://en.wikipedia.org/wiki/Computability_theory
- https://plato.stanford.edu/entries/recursive-functions/

## denotational semantics

persons/joseph-e-stoy/1977-denotational-semantics--the-scott-strachey-approach-to-programming-language-theory

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
