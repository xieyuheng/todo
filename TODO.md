# category

[category] 范畴论的一个特点是不从最基础的具体公理开始构建理论，
而是在数学实践中，在证明定理的过程中，发现理论中的 pattern 再总结成公理。

# pattern

[pattern] 读 Christopher Alexander 的书。

# clique

[clique] 增加辅助表达式。

- cicada 的设计目的是为了探索语言设计，而 clique 就是探索语言的例子，
  用想象用的 cicada-lang 重写 clique 中的探索试试。

- 通过增加辅助表达式 `(lazy)` 实现 lazy eval。
- 支持直接递归函数与相互递归函数，不能判断等价的地方就不判断。

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

# x-puzzle

[x-puzzle] expression-based puzzle games

- 把 to mock a mockingbird 做成一个游戏。
- 支持纯文字版本，因此需要 grammar

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

- 项目叫 cicada-es 代表 explicit substitution，
  需要翻新 partech 让语法解析成为稳定的舒适的存在。

  - 或者先实现一个 es 版本的 pie 或 tartlet。

  如何把 data constructor 也处理为 Exp 而不是 Value？
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
- 用 C 写，用 C 扩展。
- 用 tagged values 并支持 GC。
  - 放弃在这个项目中对 two level monoid-like type system 的探索。
  - 如果让 GC 可选，也许还可以在这里探索 linear type，
    但是不应该一次探索太多。

# geometer

[geometer] 几何学家。

- 一个醉心于几何学的人（像 Coxeter）。
- 想要渲染出他自己对几何的想象。
- 目前用 javascript 实现，最终要用 cicada 实现。
