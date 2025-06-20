# using x-data

x-data -- matcher combinators

```typescript
export function matchStmt(data: X.Data): Stmt {
  return X.matcherChoice([
    X.matcher("['define (cons name args) exp]", ({ name, args, exp }) =>
      Stmts.Define(
        X.dataToString(name),
        X.dataToArray(args)
          .map(X.dataToString)
          .reduceRight((fn, name) => Exps.Fn(name, fn), matchExp(exp)),
      ),
    ),
    X.matcher("['define (cons name args) exp]", ({ name, args, exp }) =>
      Stmts.Define(
        X.dataToString(name),
        X.dataToArray(args)
          .map(X.dataToString)
          .reduceRight((fn, name) => Exps.Fn(name, fn), matchExp(exp)),
      ),
    ),
  ])(data)
}
```

use x-data.js in cicada-lang/lambda.js

use x-data syntax to practics hindley-milner type system
use x-data syntax to practics recursive structural type

# hindley-milner type system

j-roger-hindley/1969-the-principal-type-scheme-of-an-object-in-combinatory-logic
luis-damas/1985-type-assignment-in-programming-languages--luis-damas
john-alan-robinson/1965-a-machine-oriented-logic-based-on-the-resolution-principle

j-roger-hindley/1997-basic-simple-type-theory
j-roger-hindley/2008-lambda-calculus-and-combinators--an-introduction

# combinatory logic

moses-schonfinkel/1924-on-the-building-blocks-of-mathematical-logic

> j-roger-hindley's works are based on combinatory logic

https://en.wikipedia.org/wiki/Moses_Sch%C3%B6nfinkel
https://en.wikipedia.org/wiki/Combinatory_logic
https://plato.stanford.edu/entries/logic-combinatory
https://ncatlab.org/nlab/show/combinatory+logic
https://combinatorylogic.com/

# robin milner

robin-milner/1979-edinburgh-lcf--a-mechanised-logic-of-computation
robin-milner/2009-the-space-and-motion-of-communicating-agents

# structural type

luca-cardelli/1993-subtyping-recursive-types

cicada-lang/lambda -- equal of recursive defined function mod partial evaluation

# topology and domain theory

mathematics/topology/1989-topology-via-logic--steven-vickers.djvu

# recursion theory

study recursion theory -- to understand kleene's mu operator

- https://en.wikipedia.org/wiki/mu_operator
- https://en.wikipedia.org/wiki/Computability_theory
- https://plato.stanford.edu/entries/recursive-functions/

# algebraic-subtyping

type-theory/2016-algebraic-subtyping--tephen-dolan.pdf

# kan complex

new-arrivals/2011-simplicial-structures-in-topology--davide-l-ferrario--renzo-a-piccinini.pdf
new-arrivals/2023-an-elementary-illustrated-introduction-to-simplicial-sets--greg-friedman.pdf
new-arrivals/2023-higher-categories-and-homotopical-algebra--denis-charles-cisinski.pdf
