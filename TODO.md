[todo] 整理自己对 todo 的使用，
核心 todo 必须放在醒目的位置，
时常看到。

-比如，我还需要经常看到 xvm 和 geometer。

[cicada] 一个带有 dependent type 的实用语言。

- 编译到 xvm。

- 默认没有完备性检查，也没有停机检查。

  - 也许可以选择开启这些功能。

- 适合用来探索新的语言的解释器。
  比如 inet，逻辑式编程，
  explicit substitution，
  cell comeplx 的 higher algerbra，
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

[grammar] 设计一个 DSL 专门用来描述语法 + 生成语法解析器。

- 在最开始的时候，我们还没有语法解析器，
  所以这个 DSL 没有语法解析器可用，
  所以我们可以把这个 DSL 的语法设计为 sexp-based。

- 语言只有最简单的功能，
  其抽象能力只为支持编写 grammar，
  而不为一般的编程。
  因此可能不需要支持匿名的函数 lambda（不用 closure），
  只使用在模块中定义好了的有名字的函数即可。
