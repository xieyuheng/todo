# test-runner.js

rename test-runner to test-runner.js
renew test-runner -- use commander.js and avoid using ty

# lambda-lisp.js

finishing

# occam-lisp.js

lambda-lisp.js + builtin functions

# lattice-lisp.js

recursive structural type

- use lattice-lisp as the denotational semantics of lattice-lisp, specially for type system
  - maybe use explicit substitution for runtime semantics
- use the idea of combinators -- by putting env and ctx to the last currying argument position.
- use the idea of propagator model to implement type system.
- implement not as type operator, which is needed to view pattern in pattern matching as type.

# luca cardelli

luca cardelli's work is very close to my research interests in lattice-lisp.

persons/luca-cardelli/1985-on-understanding-types-data-abstraction-and-polymorphism
persons/luca-cardelli/1987-basic-polymorphic-typechecking
persons/luca-cardelli/1989-typeful-programming
persons/luca-cardelli/1991-operations-on-records
persons/luca-cardelli/1994-an-extension-of-system-f-with-subtyping
persons/luca-cardelli/1996-a-theory-of-objects

# hindley-milner

univalent analysis of relation -- wikiepdia page of HM
