# mimor

受到 kimi 启发，重新设计 mimor 使得它的 UX 更简单。

- 在做新的 web app 之前首先要有一个稳定的数据层，
  回到 fidb 项目，这次不完全以 JSON 为 config
  来生成一个 database 的 HTTP API，
  而是用以 fidb 为 database library，
  在这之上手写 HTTP API。

- 学习 laravel + sqlite + htmx 的 web app 方案。

# 我没有时间

如果放假的时间和下班时间不写自己的项目，
上班的时候就没时间了。

# 加油！

不管是从知识积累方面，还是从设计方向方面，
cicada 项目都已经准备好了，就差努力实现了。

# learner

重新读前面的章节，获得一个完整的脉络。
就像笛卡尔所说的，经常从头到尾把问题串联起来想明白，
就可以修炼自己的思考能力和自己对问题的理解。

现在学了两种 layer 了，
用图画笔记来总结一下不同神经网络的结构。

练习手算 back propagation。

- https://www.youtube.com/watch?v=SmZmBKc7Lrs

用 propagator 构造带有复杂单元的神经网络。

- neuron 本身就可以 back propagation，所以才能学习（神经的可塑性）。
  - propagator network 可以在运行时部分反向运行。
  - 为了模仿 neuron，还可以设计遗忘机制，因为每个 cell 的容量是有限的。
    - perceptron 并不是唯一的 neuron 模型。

学了 generic 之后，可以用来学 sussman 的力学书。

学了 propagator 之后，可以用来模拟电子电路。

- 学会电子电路，是理解人类神经网络的开端之一。

# 古典

我发现学习和练习引用古典名著是很有趣的学习过程，
就像引用现代互联网上的梗很有趣的一样。

学习古典的过程其实是学习古典的 beliefs 系统的过程，
在这个过程中要择善而从，择不善而改。

但是注意要读诸子百家而不要限于经。

# 劝学

君子曰：学不可以已。

青，取之于蓝而青于蓝；冰，水为之而寒于水。

故木受绳则直，金就砺则利，君子博学而日参省乎己，则知明而行无过矣。

蓬生麻中，不扶而直；白沙在涅，与之俱黑。

积善成德，而神明自得，圣心备焉。

# 蝉语

在 clique 中实验，然后开始 cicada。

- 在 clique 中用 `assert-equal` 验证基于 `Exp` 的 definitional 等价关系。
- 在 clique 中验证基于 `Exp` 的递归函数之间的 definitional 等价关系。
- 在 clique 中验证基于 `Exp` 的 dependent type 类型检查器具。
- 在实现 explicit-substitution 时避免全局的 `globalFreshen`。

cicada 仍旧临时用 JS 实现，坚持 类-JS 语法。

XVM 作为容易实现的可扩展的编译器 target。

cicada 编译到 XVM。

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

要保持容易实现。

- 如何保持容易实现？需要 XVM？
- 想要保持容易实现，就必须用 stack-based 构架，这样就必须要求 XVM。
  - 因为只有在 stack-based + postfix 语法中，尾部递归等等概念才能简单。
  - 因此我们实现的不能是一个解释器，而必须是一个到 XVM 的编译器。
  - 为了学习 runtime 数据编码，还是要看 UI 的编译器课程。

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

# fidb

Should NOT just use file as config, should use code.
i.e. should be a library instead of db app.

# learn

读 Dan 的 language-and-programmer.pdf

- call/cc vs let-cc

  let-cc 之所以比 call/cc 更好理解，
  是因为去除了思考这个语法时的一层间接。
