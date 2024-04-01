# mugda (clique)

move mugda to clique

# pie (clique)

pie with explicit substitution.

- 当 everything is expression 时，
  inference rule 的表达会有什么变化？

  - 好像是所有论文中的 inference rule 都只会用 Exp，
    而不会用 Value 和 closure。

# typed logic programming (clique)

simply typed logic programming

dependently typed logic programming

- need equivalence between relations.
- if type system is logic, what is the logic of logic?

# logic programming (clique)

datomic-like datalog in clique

[logic programming] 尝试把多元关系转化为三元组（datomic）

- 关系的代数（peirce）

# pattern

[pattern] 读 Christopher Alexander 的书。

# grammar

[grammar] 设计一个 DSL 专门用来描述语法 + 生成语法解析器。

- 为了方便迁移到 C，应该用 lambda machine 来实现，而不是用解释器来实现。

- 在最开始的时候，我们还没有语法解析器，
  所以这个 DSL 没有语法解析器可用，
  所以我们可以把这个 DSL 的语法设计为 sexp-based。

- 语言只有最简单的功能，
  其抽象能力只为支持编写 grammar，
  而不为一般的编程。
  因此可能不需要支持匿名的函数 lambda（不用 closure），
  只使用在模块中定义好了的有名字的函数即可。

- 为了在 JS 中使用所生成的 JSON AST 可以直 evaluate grammar 的代码。
  - 作为 AST 的 Exp 和 Stmt 要写两遍，一次在 grammar 中一次在 JS 中。
  - grammar 所返回的 JSON 是不带类型的，JS 必须直接信任或额外效验。

# cicada

[cicada] 一个带有 dependent type 的实用语言。

- 编译到 xvm。

- 默认没有完备性检查，也没有停机检查。

  - 也许可以选择开启这些功能。

- 适合用来探索新的语言的解释器。
  比如 inet，逻辑式编程，
  explicit substitution，
  cell complex 的 higher algerbra，
  等等。

- 作为 dependent type 语言，
  就要在编译时带有一个解释器，
  这个解释器我们可以就尝试用
  explicit substitution 来实现。
  此时，我们不光要合并 Exp 以 Value，
  还需要合并 Exp 与 Core，
  经过 elab 所获得的 Core 也应该被囊括在 Exp 中。

- 如何把 data constructor 也处理为 Exp 而不是 Value？
  应该用 `T.C` 还是 `T::C` 作为构造数据的语法？

  - 我们还是需要 `T::C` 的，
    正如 `(lambda)` 是一个 Exp，
    通过名字引用 `(lambda)` 的时候，
    直接在查找到所对应的 Exp 就可以了
    （可能是在 mod 中，或在局部的环境中）。
    因此我们也需要一个特殊的 Exp 来表示 `T::C`，
    而不能给查找引入更复杂的机制，
    让变元的意义依赖于一个额外的参数（比如 mod）。

# xvm

[xvm] 可扩展的 VM。

- 最重要的目的是为 cicada 提供 compiler target。
  注意，这个生态位是没有标准语言的，每个动态类型语言都有自己的 VM。

- 功能：
  - 用 tagged values 并支持 GC。
  - 尾递归优化。
  - closure。
  - 用 C 写，用 C 扩展。

-  XVM 本身也可以是一个实用的脚本语言，这需要：
  - 简单类型系统。
    - 难点是需要用 C 实现。
  - 模块系统。
  - array 和 record。
  - 定义 datatype。

- 放弃在这个项目中对 two level monoid-like type system 的探索。

  - 我们有类型系统，只是没有 linear type，
    之所以放弃 linear type
    是因为我发现实现类型系统需要 closure 和 GC，
    而 linear type 很大一部分意义在于可以没有 GC。

  - 如果让 GC 可选，也许还可以在这里探索 linear type，
    但是不应该一次探索太多。

# geometer

[geometer] 几何学家。

- 一个醉心于几何学的人（像 Coxeter）。
- 想要渲染出他自己对几何的想象。
- 目前用 javascript 实现，最终要用 cicada 实现。

# category

[category] 范畴论的一个特点是不从最基础的具体公理开始构建理论，
而是在数学实践中，在证明定理的过程中，发现理论中的 pattern 再总结成公理。

# x-puzzle

[x-puzzle] expression-based puzzle games

- 把 to mock a mockingbird 做成一个游戏。
- 支持纯文字版本，因此需要 grammar

# chu

chu 楚 should be another project name -- maybe to replace geometer

# cicada syntax

fix naming convention for old examples in "the little typer"

[problem] does syntax for recursive prove (recursive function)
need motive like the `induction` keyword?

# fidb

Should NOT just use file as config, should use code.
i.e. should be a library instead of db app.
