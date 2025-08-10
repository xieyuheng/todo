# meta-lisp.js

> this is where we can test luca's idea of subtype of recursive types.

> read papers about LCF

persons/robin-milner/1984-the-use-of-machines-to-assist-in-rigorous-proof
persons/robin-milner/1972-logic-for-computable-functions-description-of-a-machine-implementation
persons/robin-milner/1976-models-of-lcf
persons/robin-milner/1978-a-metalanguage-for-interactive-proof-in-lcf
persons/robin-milner/1979-edinburgh-lcf--a-mechanised-logic-of-computation
persons/robin-milner/1979-edinburgh-lcf--a-mechanised-logic-of-computation

# luca cardelli

> luca cardelli's work is very close to my research interests in meta-lisp.

persons/luca-cardelli/1985-on-understanding-types-data-abstraction-and-polymorphism
persons/luca-cardelli/1987-basic-polymorphic-typechecking
persons/luca-cardelli/1989-typeful-programming
persons/luca-cardelli/1991-operations-on-records
persons/luca-cardelli/1994-an-extension-of-system-f-with-subtyping
persons/luca-cardelli/1996-a-theory-of-objects

persons/david-macqueen/1984-an-ideal-model-for-recursive-polymorphic-types.md

- how to view type is ideal of domain

# hindley-milner

univalent analysis of relation -- wikiepdia page of HM

# lazy evaluation and dan

read Dan's language-and-programmer.pdf

- call/cc vs let-cc
  let-cc is better than call/cc, why?
  maybe because it removed one level of indirect.

https://en.wikipedia.org/wiki/Lazy_evaluation
https://en.wikipedia.org/wiki/Daniel_P._Friedman

# lambda diagrams

it is important to have many ways to imagine lambda calculus.

https://tromp.github.io/cl/diagrams.html

# evaluation strategy

read henk-barendregt again to study evaluation strategy

persons/henk-barendregt/1984-the-lambda-calculus.pdf
persons/henk-barendregt/2010-lambda-calculus-with-types.pdf

# tree calculus

see if it is related to tree automata

topics/computer-science/tree-calculus/2021-reflective-programs-in-tree-calculus--barry-jay.pdf
webside: https://treecalcul.us

# tree automata

study/topics/computer-science/automata/tree-automata/2008-tree-automata-techniques-and-applications.pdf
study/topics/computer-science/automata/tree-automata/2015-tree-automata--ferenc-gécseg--magnus-steinby.pdf

study/topics/computer-science/automata/tree-automata/1992-tree-automata-and-languages.pdf
study/topics/computer-science/automata/tree-automata/2010-foundations-of-xml-processing--the-tree-automata-approach.pdf

# lattice theory

type system as lattice

persons/george-grätzer/1978-general-lattice-theory.md

computational analysis of formal system -- logic of finite observations

# random

[DHH: Future of Programming, AI, Ruby on Rails, Productivity & Parenting | Lex Fridman Podcast #474](https://www.youtube.com/watch?v=vagyIcmIGOQ)

persons/david-heinemeier-hansson/2006-getting-real.pdf
persons/david-heinemeier-hansson/2007-restful-web-services.pdf
persons/david-heinemeier-hansson/2018-it-doesnt-have-to-be-crazy-at-work.epub
persons/david-heinemeier-hansson/2018-it-doesnt-have-to-be-crazy-at-work.pdf

2008-the-seven-virtues-of-simple-type-theory.pdf

# combinatory-logic

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

# foundation of mathematics

learn from hilbert

- my understanding of the logic of mathematics is shaped by type theory now,
  maybe i should learn the other way.

# recursion theory

study recursion theory -- to understand kleene's mu operator

- https://en.wikipedia.org/wiki/mu_operator
- https://en.wikipedia.org/wiki/Computability_theory
- https://plato.stanford.edu/entries/recursive-functions/

# denotational semantics

persons/joseph-e-stoy/1977-denotational-semantics--the-scott-strachey-approach-to-programming-language-theory

# algebraic-subtyping

topics/type-theory/2016-algebraic-subtyping--tephen-dolan.pdf

# inet and propagator

persons/robin-milner/2009-the-space-and-motion-of-communicating-agents

# cicada

persons/peirce/1880-on-the-algebra-of-logic -- early denotational semantics for logic

# kan complex

2011-simplicial-structures-in-topology--davide-l-ferrario--renzo-a-piccinini.pdf
2023-an-elementary-illustrated-introduction-to-simplicial-sets--greg-friedman.pdf
2023-higher-categories-and-homotopical-algebra--denis-charles-cisinski.pdf

# constraint processing

结合所实现的逻辑式语言，读 "constraint processing"

# pattern

读 Christopher Alexander 的书，思考知识被固定的方式

# cell-complex

回顾 cell-complex + cobordism + lisp 的项目 -- 实现几何引擎

# study

topics/computer-science/interaction-nets/the-optimal-implementation-of-functional-programming-languages--andrea-asperti.pdf
projects/others/HigherOrderCO/HVM/paper/HVM2.pdf
[maybe] persons/jean-yves-girard/proof-nets--the-parallel-syntax-for-proof-theory--1995.pdf

2017-arithmetic.pdf -- what is computation
2012-measurement.pdf
2009-the-existential-graphs-of-charles-s-peirce--don-d-roberts.djvu
2006-proof-nets-and-the-identity-of-proofs--straßburger.pdf
2023-essentials-of-compilation-racket.pdf

# projects

propagator -- a language for propagator model -- to experiment with type checking
"essentials of compilation" -- learn about compilation -- using x-forth
learn pytorch and tinygrad -- tinygrad v.s. little learner
readonly.link -- be like sourcehut

# category

[category] 范畴论的一个特点是不从最基础的具体公理开始构建理论，
而是在数学实践中，在证明定理的过程中，发现理论中的 pattern 再总结成公理。

# x-puzzle

[x-puzzle] expression-based puzzle games

- 把 to mock a mockingbird 做成一个游戏。
- 支持纯文字版本，因此需要 grammar

# fidb

Should NOT just use file as config, should use code.
i.e. should be a library instead of db app.

# mimor

受到 kimi 启发，重新设计 mimor 使得它的 UX 更简单。

- 在做新的 web app 之前首先要有一个稳定的数据层，
  回到 fidb 项目，这次不完全以 JSON 为 config
  来生成一个 database 的 HTTP API，
  而是用以 fidb 为 database library，
  在这之上手写 HTTP API。
