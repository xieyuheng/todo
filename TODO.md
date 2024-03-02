[geometer] move cell complex code to `geometer`

[geometer] 几何中的很多分类问题，
可能也等价于 normalization 问题，
即通过 normalization 来给一个集合的分类，

- 如何用这种观点去理解 the-symmetries-of-things 中的分类？
  是否像 lambda 演算一样，应该先有表达式再有 reduction to normal form？

[geometer] 几何学家

- 一个醉心于几何学的人，喜欢几何学的各个领域，像 Coxeter 等人。
- 要能渲染出他自己对几何的想象。
- 目前用 javascript 实现，最终要用 cicada 实现。

[cicada] 一个带有 dependent type 的实用语言。

- 编译到 xvm。

- 默认没有完备性检查，也没有停机检查。

- 适合用来探索新的语言的解释器。
  比如 inet，逻辑式编程，
  explicit substitution，
  cell comeplx 的 higher algerbra，
  等等。

[xvm] 可扩展的 vm。

- 用 c 实现，用 c 扩展。
- 实用 tag value，带有 GC。
