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

# note

- call/cc vs let-cc

  let-cc 之所以比 call/cc 更好理解，
  是因为去除了思考这个语法时的一层间接。
