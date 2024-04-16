# chimera

[chimera] 完成更多的 clause-and-effect 中的例子。

[chimera] 关于 logic programming 与 first-order logic 的笔记。

- `clause` 中的 variable 代表 `forall`。
- `find` 代表 `exists`。

[chimera] CLP 中的 `Relation` 与 `Constraint` 的语义都是集合论意义上的 relation。

- 它们有什么区别？
- 为什么我们需要 `Constraint` 而不能用 `Relation` 实现全部？

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

- XVM 本身也可以是一个实用的脚本语言，这需要：
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

# pattern

[pattern] 读 Christopher Alexander 的书。

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
