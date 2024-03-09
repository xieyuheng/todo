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
