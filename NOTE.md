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

# learn

读 Dan 的 language-and-programmer.pdf

- call/cc vs let-cc

  let-cc 之所以比 call/cc 更好理解，
  是因为去除了思考这个语法时的一层间接。
